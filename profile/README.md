# Offering Discovery Protocol

The Offering Discovery Protocol (ODP) enables Agents to discover Services and navigate the
Collections, Offerings, and Actions they expose. It supports everything from a Service with a small
static catalog to a marketplace with a large, searchable catalog and Service-defined structured
data.

ODP is an open protocol with public specifications, schemas, examples, test vectors, conformance
artifacts, and software development kits. A Service publishes a well-known ODP document that tells
an Agent which catalog operations are available and where to call them.

## How ODP works

1. An Agent searches the canonical Directory for relevant Services.
2. The Agent inspects a Service's live ODP document and its advertised capabilities.
3. The Agent lists or searches Collections and Offerings using only the operations that Service
   supports.
4. The Agent retrieves complete Offering details and can resolve an advertised Action before
   enrollment or payment.

The Directory contains searchable Service metadata. Product catalogs remain with their Services,
allowing each Service to control its catalog, availability, access requirements, and structured
Offering data.

## Protocol composition

ODP provides agentic discovery: what a Service offers and how an Agent can navigate it. It composes
with the Agent Enrollment Protocol (AEP) for agentic enrollment and with MPP or x402 for agentic
payments.

These layers can be used independently, but together they provide a complete agentic commerce flow:
an Agent discovers an Offering, enrolls when the Service requires an identity or credential, and
pays through the payment protocol accepted by the Action endpoint.

## Start here

| Goal                              | Resource                                                                              |
| --------------------------------- | ------------------------------------------------------------------------------------- |
| Learn the protocol                | [ODP documentation](https://www.offeringprotocol.org/)                                |
| Discover Services                 | [Canonical Directory](https://directory.inflowpay.ai/)                                |
| Integrate a Service               | [Service integration guide](https://directory.inflowpay.ai/integrate/)                |
| Validate a Service                | [Service validator](https://directory.inflowpay.ai/validate/)                         |
| Use ODP from an Agent or terminal | [InFlow CLI](https://www.inflowcli.ai/)                                               |
| Discuss protocol design           | [`odp-specs` Discussions](https://github.com/offering-protocol/odp-specs/discussions) |

## Repositories

| Repository                                                      | Purpose                                                          |
| --------------------------------------------------------------- | ---------------------------------------------------------------- |
| [`odp-specs`](https://github.com/offering-protocol/odp-specs)   | Specifications, schemas, examples, test vectors, and conformance |
| [`odp-node`](https://github.com/offering-protocol/odp-node)     | Node.js software development kit and reference implementation    |
| [`odp-go`](https://github.com/offering-protocol/odp-go)         | Go software development kit                                      |
| [`odp-java`](https://github.com/offering-protocol/odp-java)     | Java software development kit                                    |
| [`odp-python`](https://github.com/offering-protocol/odp-python) | Python software development kit                                  |
| [`odp-rust`](https://github.com/offering-protocol/odp-rust)     | Rust software development kit                                    |

Protocol proposals and wire-format discussions belong in `odp-specs`. Implementation bugs and
language-specific integration questions belong in the corresponding software development kit
repository.
