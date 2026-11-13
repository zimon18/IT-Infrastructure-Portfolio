# School Network Design

A school network proposal for five computer labs on one floor. The design combines a logical topology, a structured cabling plan, equipment selection, a basic security section, an implementation schedule, and a historical cost estimate.

## Requirements

- Connect five labs with at least 16 student workstations each (80 computers total).
- Provide internet access, a shared network printer, internal DNS, and access to a school intranet site.
- Keep the server and central network equipment in a rack in one of the labs.
- Provide wired connectivity; Wi-Fi was outside the project scope.

## Proposed design

- Cisco Packet Tracer logical topology with a router, seven switches, and one server.
- Six VLANs and corresponding /24 subnets: five lab networks and a separate server network.
- Gigabit Ethernet to end devices.
- One central distribution point and five smaller distribution points.
- Rack-mounted router, switch, patch panel, server, and UPS at the main distribution point.
- A documented equipment list, work estimate, and historical total estimate of **PLN 40,055.79 gross**.

## Project document

The full 42-page Polish design document, including floor plans, logical and physical topology diagrams, addressing, equipment research, and costing, is available as [`school-network-design-pl.pdf`](school-network-design-pl.pdf).

## My contribution

I prepared the school network proposal and its documentation: gathered the requirements, planned the logical segmentation and addressing, mapped equipment and distribution points, and assembled the cost and work estimates. This is a design exercise; it does not claim that the network was installed or operated in production.

## Limitations

The document is an academic design, not an implementation record. Hardware prices and product availability reflect the time of the original project and are not current quotes. The security section is introductory and does not constitute a complete security architecture. The source document is in Polish.
