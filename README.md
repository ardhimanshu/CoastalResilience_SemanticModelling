# Coastal Resilience Semantic Knowledge Graph modelling

Work on semantic knowledge graph for coastal resilence. This project is a first step at modelling coastal resilience across Pacific Island countries, using the example text on Fiji, Tonga, Vanuatu, Nature-based Solutions, SPC-led capacity building, community engagement, monitoring, and restoration practice.

## Files

- `coastal_resilience_kg.ttl` — Turtle RDF file containing the ontology and example instance data.
- `coastal_resilience_kg.rdf` — RDF/XML serialization of the same graph.
- `coastal_resilience_ontology.owl` — OWL/RDF ontology file, usable in Protégé and other OWL tools.
- `README_coastal_resilience_kg.md` — this guide.

## What this graph represents

The model connects:

- **Places**: Pacific, Pacific Island countries, Fiji, Tonga, Vanuatu, Nadiri restoration site.
- **Hazards and pressures**: rising seas, storm surges, saltwater intrusion, shoreline erosion.
- **Interventions**: Nature-based Solutions, mangrove restoration, coral reef rehabilitation.
- **Actors**: SPC, SPREP, IUCN, GGGI, ministries, civil society organisations, communities, customary landowners.
- **Activities**: capacity needs assessment, regional training exchange, field visit, monitoring, planning.
- **Capacities**: technical capacity, implementation capacity, monitoring capacity, community engagement capacity.
- **Knowledge types**: science, local knowledge, traditional knowledge.
- **Outcomes**: coastal resilience, shoreline stability, ecosystem recovery, biodiversity support, fisheries support, community wellbeing.

## Core semantic idea

The graph treats coastal resilience not as a single flat concept, but as an outcome produced through relationships among hazards, ecosystems, communities, institutions, capacities, tools, and interventions.

A simplified pattern is:

```text
Hazard or pressure -> contributes to -> Impact
Impact -> affects -> Community or ecosystem
Intervention -> addresses hazard -> Hazard or risk
Intervention -> supports outcome -> Outcome
Training -> strengthens capacity -> Capacity
Organisation -> delivers/supports/funds -> Activity
Tool or method -> monitors indicator -> Indicator
Indicator -> helps measure -> Outcome
```

## Example RDF triple

```turtle
cr:MangroveRestoration cr:addressesHazard cr:CoastalRisk .
```

This means:

```text
Mangrove restoration -> addresses hazard -> coastal risk
```

## Future for this knowledge graph depending on project direction

Future additions depending on project direction:

1. Add more countries and coastal sites.
2. Add more Nature-based Solutions, such as seagrass restoration, dune restoration, wetland protection, watershed restoration, and ridge-to-reef approaches.
3. Add datasets for indicators, such as shoreline change, mangrove cover, coral health, fishery productivity, and community wellbeing.
4. Add temporal data: intervention start date, monitoring date, restoration phase, and project duration.
5. Add evidence links: reports, articles, datasets, field notes, monitoring forms, and training materials.
6. Add provenance: who asserted a statement, from which source, and when.
7. Add uncertainty: whether a relationship is observed, assumed, planned, or evidence-backed.

## Important note:

- It is understood and cautioned that communities are not treated only as beneficiaries. They can also be knowledge holders, landowners, implementation partners, and monitors.
- “Capacity” is not one generic concept here. There can be separate capacities - technical, institutional, monitoring, planning, and community engagement capacities.
- Mangroove restoration is just an instance of Nature-based Solutions (NbS). In larger scope of the project, NbS would be broad and extensible.
- Still deliberating on predicates like `relatedTo`. IT may be used early in the exploration process but need to be thoroughly deliberated for later stages
- Source metadata will be added further as the graph grows.

## Namespace

example.org has been used here but it is to be replaced with actual domain:

```text
https://example.org/coastal-resilience#
```

