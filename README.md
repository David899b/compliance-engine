# compliance-engine

**DPAs/Regulations → Executable Test Suites**

Converts DPAs, contracts, and regulations (Ley 25.326, GDPR, EU AI Act) into executable pytest test suites + immutable audit trails.

## Features
- Ingests DPAs, contracts, regulations via LLM
- Extracts atomic obligations → maps to executable test cases
- Generates pytest test suites + compliance dashboard
- Immutable audit trails (SHA-256)
- Supports: Ley 25.326 (Argentina), GDPR, EU AI Act
- Plugin architecture for new regulations

## Quick Start
```bash
pip install compliance-engine
compliance-engine ingest --regulation gdpr --output tests/compliance/
compliance-engine audit --run-id latest
```

## Architecture
```
ingest/     # LLM-based obligation extraction
generate/   # pytest test case generation
audit/      # Immutable audit trails (SHA-256)
dashboard/  # Compliance dashboard (Streamlit)
plugins/    # Regulation-specific plugins
```

## License
MIT License — Copyright (c) 2026 David Bautista
