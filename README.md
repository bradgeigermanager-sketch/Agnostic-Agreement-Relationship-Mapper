AARM‑v2.0 — Agnostic Agreement & Relationship Mapper

Dual‑Manifold Mesh Edition

AARM‑v2.0 is a distributed legal‑logic engine that computes net permissions for entities governed by overlapping jurisdictions. It operates simultaneously in:

- Semantic Manifold (RDF/OWL)  
- Symbolic Manifold (Atomic JSON)  

and synchronizes across distributed agents using a mesh‑native fixpoint protocol.

---

🚀 Features

- Dual‑manifold data model (RDF + Atomic JSON)  
- Conflict resolution via Lex Superior / Specialis / Posterior  
- Deterministic Resolution Records  
- SHACL structural validation  
- SWRL inference layer  
- Mesh ontology integration  
- Distributed fixpoint convergence  
- Mesh Agent runtime  
- Message bus specification  

---

📂 Repository Structure

AARM-v2.0/
│
├── README.md
├── LICENSE
│
├── docs/
│   ├── architecture-overview.md
│   ├── dual-manifold-design.md
│   ├── fixpoint-protocol.md
│   ├── message-spec.md
│   ├── swrl-rule-layer.md
│   ├── shacl-suite.md
│   ├── mesh-ontology.md
│   └── resolution-records.md
│
├── ontology/
│   ├── aarm-mesh-ontology.ttl
│   └── aarm-mesh-context.jsonld
│
├── shacl/
│   └── aarm-shapes.ttl
│
├── swrl/
│   └── aarm-rules.swrl
│
├── schemas/
│   ├── entity.schema.json
│   ├── agreement.schema.json
│   ├── event.schema.json
│   ├── resolution-record.schema.json
│   └── mesh-metadata.schema.json
│
├── atomic/
│   └── (empty placeholder; agents populate this)
│
├── src/
│   ├── aarm_graph_generator.py
│   ├── aarm_permission_generator.py
│   ├── aarm_runtime_engine.py
│   ├── aarm_mesh_agent.py
│   └── utils/
│       ├── hashing.py
│       ├── signing.py
│       └── jsonld_loader.py
│
├── examples/
│   ├── ENT-001.json
│   ├── AGR-001.json
│   ├── EVT-001.json
│   └── sample-permission-query.json
│
└── tests/
    ├── test_ingestion.py
    ├── test_permission_engine.py
    ├── test_fixpoint.py
    ├── test_agent.py
    └── test_shacl_validation.py

---

🧠 Core Components

Ontology
Located in ontology/:

- aarm-mesh-ontology.ttl — full OWL ontology  
- aarm-mesh-context.jsonld — JSON‑LD context for atomic nodes  

SHACL Suite
Located in shacl/:

- aarm-shapes.ttl — structural validation for all node types  

SWRL Rule Layer
Located in swrl/:

- aarm-rules.swrl — hierarchy, specificity, chronology rules  

Schemas
Located in schemas/:

- Entity, Agreement, Event, ResolutionRecord, MeshMetadata  

Runtime Engine
Located in src/:

- aarmruntimeengine.py — orchestrates ingestion, inference, fixpoint, export  
- aarmpermissiongenerator.py — computes net permissions  
- aarmgraphgenerator.py — RDF + JSON dual‑manifold builder  
- aarmmeshagent.py — distributed mesh agent  

Message Bus Spec
Located in docs/message-spec.md.

Fixpoint Protocol
Located in docs/fixpoint-protocol.md.

---

🧪 Tests

Located in tests/:

- Ingestion  
- Permission engine  
- Fixpoint convergence  
- Agent behavior  
- SHACL validation  

---

🧬 Example Usage

`python
from src.aarmgraphgenerator import AARMGraphGenerator
from src.aarmpermissiongenerator import AARMPermissionGenerator
from src.aarmruntimeengine import AARMRuntimeEngine

graph = AARMGraphGenerator()
perm = AARMPermissionGenerator(graph)
engine = AARMRuntimeEngine(graph, perm)

result = engine.run("ENT-001", "OperateDrone")
print(result)
`

---

📄 License

MIT
