# Order Reliability Sprint

[Broker integration review](#what-we-check) · [Roofing and HVAC estimate review](FIELD-SERVICE.md) · [Trading platform technology](PLATFORM-TECHNOLOGY.md)

**One broker integration. Four failure scenarios. Ten business days.**

Robert Hampton offers a fixed-scope, AI-assisted engineering review for
teams that route orders to brokers. The introductory engagement is
**USD 2,500**. Qualification, scope, questions and findings are handled
in writing.

## What we check

1. **Duplicate delivery.** Does replaying an execution count it twice?
2. **Reconnect gaps.** Can the application recover a fill it missed?
3. **Cancel and fill races.** Does the application record fills while a
   cancel request is pending and reconcile the final quantities?
4. **Submission timeouts.** Can the application identify an accepted
   order by client order ID before deciding whether a retry is safe?

## What you receive

Replay fixtures with instructions, a report tracing each result to its
evidence, prioritized findings with suggested fixes, and a written
readout. Each agreed case is marked **passed**, **failed** or
**unverified**. Follow-up questions stay in the same written thread.

### Example findings from a synthetic replay

| Scenario | Broker filled shares | Application filled shares | Finding |
| --- | ---: | ---: | --- |
| Duplicate delivery | 10 | 20 | Review. The application counted execution F101 twice. |
| Fill missed on reconnect | 10 | 4 | Review. Execution F202 accounts for the missing six shares. |
| Partial fill during cancellation | 3 | 3 | Matched. Both records show three shares filled and the balance canceled. |
| Submission timed out | 0 | 0 | Matched. The client order ID resolved to an open broker order. |

These are fictional orders. Each finding in the pilot cites the records
that support it or identifies the evidence still needed.

## How the engagement starts

We agree in writing on one integration, the four scenarios, expected
order and fill behavior, input coverage, acceptance and payment terms.
The ten-business-day delivery period begins after written scope approval
and receipt of the complete agreed inputs. Your team runs any sandbox
checks that require credentials and supplies the results or paired redacted
application and broker exports. Keep live credentials and customer
identifiers out of the engagement. Your team owns formal certification
and go-live.

## Request a written scope

[Request a broker pilot scope](mailto:orderreliabilitysprint@gmail.com?subject=Broker%20order%20reliability%20pilot&body=Hi%20Robert%2C%0D%0A%0D%0AI%27d%20like%20to%20discuss%20this%20pilot.%0D%0A%0D%0ABroker%20or%20adapter%3A%20%0D%0AOrder-state%20problem%20to%20review%3A%20%0D%0AAvailable%20evidence%20%28sandbox%20results%20or%20redacted%20exports%29%3A%20%0D%0AEngineering%20reviewer%20and%20target%20date%3A%20%0D%0ACommissioning%20team%2C%20if%20known%3A%20%0D%0AWhere%20did%20you%20find%20this%20offer%3F%20%28optional%29%20). If you write from your email app, use **orderreliabilitysprint@gmail.com** and the subject **Broker order reliability pilot**.
Start with a high-level summary. Keep live credentials and customer
identifiers out of the inquiry. Send any walkthrough questions in the
same email thread.

Robert Hampton | Order Reliability Sprint

## Review for roofing and HVAC offices

The separate [open estimate review pilot](FIELD-SERVICE.md) covers one
office's existing estimate queue, with a USD 1,500 fixed introductory fee
and five business days after written approval and complete agreed inputs.

## Trading platform technology

The separate [trading technology discussion](PLATFORM-TECHNOLOGY.md)
covers proposed software subscriptions, component licensing and a defined
technology sale. A customer release and hosted service are in preparation;
start with a written fit discussion about one workflow.
