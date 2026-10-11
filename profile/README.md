# LLM Measurement

Why did LLM token usage spike? Which users drove it? How do you keep those
answers without a Prometheus label for every user?

We build open-source tools for answering these questions locally: fleetdiff for
investigation, an OpenTelemetry Collector connector for continuous measurement,
and llm-sketchkit for Go services and Python analysis.

**Guides with runnable examples:** [llm-measurement.github.io](https://llm-measurement.github.io/).

## Start With Your Question

| Your question | Start here |
| --- | --- |
| Can my traces answer questions about users, sessions and token usage? | [fleetdiff inspect](https://github.com/llm-measurement/fleetdiff/blob/main/docs/INSPECT.md) checks a local OTLP capture and shows what to add. |
| Which user or session is driving my LLM token spike? | [fleetdiff investigate](https://github.com/llm-measurement/fleetdiff/blob/main/docs/INVESTIGATION.md) compares two windows and identifies leading contributors. |
| Which windows show unusual token consumption? | [fleetdiff scan](https://github.com/llm-measurement/fleetdiff/blob/main/docs/SCAN.md) reports usage, coverage and contributor changes against a recent baseline. |
| Will this collector config turn user IDs into metric labels? | [fleetdiff diagnose](https://github.com/llm-measurement/fleetdiff/blob/main/docs/DIAGNOSE.md) points to risky labels and unsupported settings. |
| How do I avoid Prometheus cardinality explosion in LLM metrics? | [otelcol-genai-sketches](https://github.com/llm-measurement/otelcol-genai-sketches) turns spans into metrics and keyed user/session rankings, while keeping your trace backend. |
| How do I count distinct users and find token-heavy keys in my own code? | [llm-sketchkit](https://github.com/llm-measurement/llm-sketchkit) provides mergeable measurements in Go and Python. |

## Using LiteLLM?

Start with the [LiteLLM telemetry recipe](https://github.com/llm-measurement/otelcol-genai-sketches/tree/v0.3.1/examples/integrations/litellm).
It compares reported usage before and after a change using collector summaries.
For a quick synthetic example, run [fleetdiff's session comparison](https://github.com/llm-measurement/fleetdiff/tree/main/examples/sessions).

Working in Python? Start with `python -m pip install llm-sketchkit` and the
[Python example](https://github.com/llm-measurement/llm-sketchkit#python).

## Share One Useful Result

[Share your inspect headline](https://github.com/llm-measurement/fleetdiff/discussions/20).
The gateway or framework version helps too. Keep raw traces, prompts, identifiers
and credentials private.

Questions are welcome in each repository. Follow its SECURITY.md for private
vulnerability reports.
