# LLM Measurement

LLM Measurement builds open-source tools for understanding LLM usage: what changed, who drove it, and whether the usage records support the answer. They run in your own environment on telemetry you already collect, and keep raw user IDs out of their outputs.

- **[fleetdiff](https://github.com/llm-measurement/fleetdiff)**: a local command-line tool that explains token-usage changes, including directly from LiteLLM spend exports, flags unusual windows, and checks trace captures and collector configurations.
- **[otelcol-genai-sketches](https://github.com/llm-measurement/otelcol-genai-sketches)**: an OpenTelemetry Collector connector that tracks token usage by user, session and model without a metric label for every user.
- **[llm-sketchkit](https://github.com/llm-measurement/llm-sketchkit)**: a Go and Python library that counts distinct users and ranks the heaviest users by tokens, in small summary files.

**Guides with runnable examples:** [llm-measurement.github.io](https://llm-measurement.github.io/)

Questions are welcome in each repository. Report vulnerabilities privately through each repository's SECURITY.md.
