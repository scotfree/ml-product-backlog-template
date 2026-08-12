# Epic: Corpus (Ag-Bot-CV)

## What this epic covers

Public agricultural CV datasets — one per detection task. LaboroTomato for fruit/ripeness, IP102 for pest, PlantVillage/PlantDoc/FieldPlant for disease. License audit matters here: some datasets have non-commercial restrictions that would block AgCloud deployment.

## Cards in this epic

1. Identify candidate datasets
2. Characterize the chosen dataset
3. Split train / validation / test with a rationale

## Success criteria

One license-cleared dataset chosen per task, characterized in a committed notebook, with seeded splits in code — including the cross-dataset disease split that Sprint 5's lab-to-field eval depends on. Demoable as the IP102 long-tail histogram and the assertion that blocks test-set leakage.
