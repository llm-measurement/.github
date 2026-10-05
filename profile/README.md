# LLM Measurement

Open-source tools for understanding token usage and agent traffic without
indexing every prompt, user, or session.

## Start With A Question

| Your question | Start here |
| --- | --- |
| Can my traces answer the questions I care about? | [fleetdiff inspect](https://github.com/llm-measurement/fleetdiff/blob/main/examples/inspect/README.md) checks a local trace file and shows what to add next. |
| Why did my app's token usage change? | [fleetdiff investigate](https://github.com/llm-measurement/fleetdiff/blob/main/docs/INVESTIGATION.md) compares before and after, showing changes in model attempts, tokens per attempt, caching, and tracked contributors. |
| Which recent windows need attention? | [fleetdiff scan](https://github.com/llm-measurement/fleetdiff/blob/main/docs/SCAN.md) flags unusual usage, coverage, and contributor changes, with a reason for each flag. |
| Is my collector configuration ready to use? | [fleetdiff diagnose](https://github.com/llm-measurement/fleetdiff/blob/main/docs/DIAGNOSE.md) checks supported settings, finds risky metric labels, and points to what needs fixing. |
| How do I keep collecting useful measurements without a metric label for every user? | [otelcol-genai-sketches](https://github.com/llm-measurement/otelcol-genai-sketches) turns OpenTelemetry spans into counters, distinct estimates, and ranked keyed summaries. Keep your existing telemetry backend. |
| How do I build these measurements into my own service or notebook? | [llm-sketchkit](https://github.com/llm-measurement/llm-sketchkit) provides mergeable sketches in Go and Python, with a shared format and explicit error bounds. |

Use each project on its own, or collect summaries with the connector and compare
them with fleetdiff. The library also works directly in services and notebooks.

## Try One

- **Have a trace file?** Follow the [capture and inspect recipes](https://github.com/llm-measurement/fleetdiff/blob/main/examples/inspect/README.md).
- **Want a working demo?** Try the [collector demo](https://github.com/llm-measurement/otelcol-genai-sketches#quick-start), with Prometheus and Grafana.
- **Working in Python?** Start with `python -m pip install llm-sketchkit` and the [Python example](https://github.com/llm-measurement/llm-sketchkit#python).

## Help With One Small Thing

[Share your inspect headline](https://github.com/llm-measurement/fleetdiff/discussions/20).
One line is enough; your gateway or framework version is useful too. Please
leave out raw traces, prompts, identifiers, credentials, and customer details.

For a first contribution, try a
[gateway capture recipe or configuration check](https://github.com/llm-measurement/fleetdiff/issues?q=is%3Aissue%20is%3Aopen%20label%3A%22good%20first%20issue%22).
Bug reports and questions are welcome in each repository. Use its `SECURITY.md`
for private vulnerability reports.
