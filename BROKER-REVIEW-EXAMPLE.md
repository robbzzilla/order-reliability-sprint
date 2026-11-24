# Fictional broker reliability report

This is an example of a written findings report. It covers one fictional
adapter and four synthetic scenarios. The observations below belong to
the example. They convey no finding about a live broker or customer.

| Case | Expected result | Evidence in the example | Finding |
| --- | --- | --- | --- |
| R1 Duplicate delivery | One fill for execution F101 | The broker shows F101 for 10 shares. The application books F101 for 10 shares twice. | Failed. The execution contributes twice to the application total. |
| R2 Reconnect recovery | Every execution appears after reconnection | The broker shows 10 shares filled, including six on F202. The application shows four shares and omits F202 in the covered batch. | Failed. F202 accounts for the six missing shares. |
| R3 Fill during cancellation | Record the fill and the canceled balance | Both records show three shares filled and the remaining quantity canceled. | Passed for the sample quantities and final status. |
| R4 Submission timeout | Resolve the lost response against the original client order ID | The original ID resolves to one open broker order with zero fills, consistent with the application quantity. | Order match verified. A send journal is still needed to verify whether the application attempted a second submission. |

In R2, a report with missing or uncertain coverage would leave recovery
unverified. In R4, a zero fill count by itself leaves the order state
unverified. Check the original ID and the broker order state.

## Written retest

- For R1, replay the same execution. Check the individual execution ID
  and the position change after both deliveries.
- For R2, compare the before- and after-reconnect evidence against the
  broker record. Agree on the scope and cutoff before drawing a finding.
- For R3, retain the fill and cancellation records. Compare the filled
  quantity and final remaining quantity on both sides.
- For R4, retain the original client order ID, broker lookup result and
  redacted send journal. Check the number of submissions separately
  from order matching.

The introductory review is **USD 2,500** for one adapter. The ten-business-day
period begins after written approval and receipt of the complete agreed
inputs. The buyer runs credentialed sandbox checks and owns certification
and go-live. [Request a written scope](README.md#request-a-written-scope).
