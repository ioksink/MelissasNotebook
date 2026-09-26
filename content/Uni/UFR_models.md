---
title: "Uni Freiburg OpenWebUI Models"
date: 2026-08-13
draft: false
---

# Which model should I choose from the current list of models provided by uni freiburg openwebui?

Several identifiers appear to be institutional aliases or future/internal names rather than publicly documented model releases. Therefore, the recommendations below are inferred from the displayed name, model family, size, and routing category—not verified benchmark results. In particular, the exact differences among GPT 5.6 Terra, Luna, and Sol, or between Standard and UFR routes, depend on your provider’s configuration.

Also, the supplied configuration has malformed indentation: each `name` should align with its corresponding `title`. The last two entries reuse `standard-chat-ufr` as their title, which may make them difficult to distinguish in a UI.

## Best use case for every entry

| Displayed model | Best use case | Coding | Academic writing |
|---|---|---:|---:|
| **UFR: Standard Chat** | Everyday questions, summaries, rewriting, brainstorming, and general assistance | Good for small tasks | Good for routine drafting |
| **UFR: Standard Reasoning** | Multi-step analysis, planning, interpreting evidence, and difficult conceptual questions | Very good for debugging/design | Very good for argument development |
| **UFR: Standard Coding** | General software development, code explanation, refactoring, tests, and bug fixes | **Excellent default** | Limited except technical material |
| **UFR: Standard Vision** | Understanding screenshots, figures, diagrams, scanned pages, and image-based questions | Useful for UI/error screenshots | Useful for figures and page review |
| **UFR: Gemma 4 31B** | Higher-quality general work where an open-model route is preferred; drafting, analysis, and multilingual text | Good | Very good, subject to validation |
| **UFR: Gemma 4 12B** | Faster/lighter general assistance, summarization, extraction, and straightforward drafting | Fair–good | Good for editing and outlines |
| **UFR: Gemma3 27b** | General open-model chat, summarization, writing, and possibly vision if enabled by the provider | Good | Good–very good |
| **UFR: Mistral Small 4** | Fast everyday assistance, concise summaries, extraction, classification, and modest coding tasks | Good for localized changes | Good for editing; less ideal for deep synthesis |
| **UFR: nuExtract3 (OCR)** | Extracting structured content from scans, PDFs, forms, tables, receipts, and images | Not intended | Useful only to recover source text/data |
| **UFR: Numarkdown 8b Thinking** | Turning complex documents into clean Markdown while preserving headings, lists, tables, equations, or layout | Not a primary coder | Excellent document-preparation tool, not an essay author |
| **UFR: GLM 5.2** | Broad reasoning, coding, and writing, but marked for retirement | Potentially strong | Potentially strong, but avoid for new workflows |
| **UFR: Qwen 3.5 397B / A17B** | Demanding reasoning, multilingual work, difficult coding, long-form synthesis, and complex instructions | **Excellent candidate** | **Excellent candidate** |
| **UFR: Qwen 3.6 27B** | Mid-sized general reasoning/coding model, but marked for retirement | Very good candidate | Very good candidate; avoid new dependencies |
| **UFR: GPT-OSS 120B / A11B** | Strong open-model reasoning, code review, analysis, structured generation, and general writing | **Very good–excellent** | Very good for planning/revision |
| **Mistral Large Latest** | High-quality general reasoning, multilingual writing, synthesis, and complex instructions | Very good | **Excellent candidate** |
| **Codestral Latest** | Code completion, repository work, refactoring, debugging, test generation, and code review | **Excellent specialist** | Poor choice for prose unless the essay is code-centric |
| **OpenAI: GPT 5.6 Terra** | Presumably a high-capability GPT route; difficult reasoning, large code changes, or advanced synthesis | Likely excellent | Likely excellent, but route details are needed |
| **OpenAI: GPT 5.6 Luna** | Presumably a balanced GPT route for general professional work | Likely excellent | Likely excellent, but route details are needed |
| **OpenAI: GPT-5.4** | Advanced reasoning, coding, synthesis, and writing; marked for replacement | Excellent candidate | Excellent candidate; avoid new long-term dependency |
| **UFR: Qwen 3.5 9b (no reasoning)** | Fast, inexpensive transformations, short answers, classification, boilerplate, and simple edits | Fair for simple snippets | Fair for proofreading; weak for argumentation |
| **UFR: Chat** | Automatic/default chat routing when you do not want to choose a specific model | Good general fallback | Good general fallback |
| **UFR: Text** | Text-only generation, rewriting, summarization, extraction, and classification | Limited–good | Good for prose transformations |
| **UFR: Reasoning Fast** | Quick analysis, modest debugging, comparisons, and planning with lower latency | Very good for routine problems | Very good for outlines and critique |
| **UFR: Reasoning Complex** | Hard multi-step problems, methodological analysis, difficult debugging, and careful decision-making | **Excellent for hard bugs/design** | **Excellent for logic and synthesis** |
| **UFR: Vision Fast** | Rapid OCR-like questions, screenshot interpretation, and simple figure inspection | Good for quick UI diagnostics | Good for quick chart inspection |
| **UFR: Vision Complex** | Dense figures, scientific plots, multi-panel images, diagrams, or nuanced visual reasoning | Very good for architecture/UI analysis | **Best vision route for scientific figures** |
| **UFR: Coding Fast** | Autocomplete-like tasks, isolated functions, small fixes, formatting, and simple tests | **Excellent for quick edits** | Not recommended |
| **UFR: Coding Complex** | Cross-file refactoring, architecture, difficult bugs, migrations, performance analysis, and comprehensive tests | **Best routed coding option** | Only for technical sections/code methods |
| **UFR: Chat Fast** | Low-latency questions, short rewrites, and uncomplicated summaries | Fair–good | Good for proofreading |
| **UFR: Chat Standard** | Balanced everyday chat with better quality than the fastest route | Good | Very good for ordinary drafting/editing |
| **UFR: Vision Standard** | Balanced image understanding for screenshots, plots, and documents | Good | Very good for figure interpretation |
| **OpenAI: GPT 5.6 Sol** | Presumably another GPT capability/latency tier; use according to local Terra/Luna/Sol documentation | Likely excellent | Likely excellent, but exact ranking is unknown |
| **UFR: GLM 5.3 Flash** | Fast, economical chat, summarization, extraction, translations, and small coding questions | Good for small tasks | Good for editing, less suitable for deep scholarship |
| **UFR: Qwen-3.8-27b** | Mid-sized multilingual general model; likely balanced reasoning, coding, and writing | Very good candidate | Very good candidate |

## Best choices for coding improvements

### Recommended order

1. **UFR: Coding Complex** — best first choice for reviewing and improving an existing project, especially cross-file refactoring, architecture, difficult bugs, and test strategy.
2. **Codestral Latest** — best named specialist for implementation, completion, refactoring, and code review.
3. **UFR: Standard Coding** — safest balanced default when the complexity is unclear.
4. **UFR: Qwen 3.5 397B / A17B** — promising for tasks combining difficult reasoning with code, such as algorithm redesign or diagnosing subtle behavior.
5. **UFR: Reasoning Complex** — use when understanding the root cause or architecture matters more than rapidly producing code.
6. **GPT 5.6 route** — likely appropriate for sophisticated repository work, but choose Terra, Luna, or Sol only after checking your institution’s route descriptions.
7. **UFR: Coding Fast** — best for small, well-scoped patches and test generation where speed matters.

A practical workflow is:

- **Coding Fast** for tiny edits.
- **Standard Coding** for ordinary feature work.
- **Coding Complex** for repository-wide or risky changes.
- **Reasoning Complex** for diagnosis and design before implementation.
- **Codestral** when you specifically want a code-specialized model.

For reliable improvements, provide the relevant files, runtime and dependency versions, expected behavior, tests, and constraints. Ask the model to explain risks and produce tests rather than accepting an unverified rewrite.

## Best choices for academic essays

### Recommended order

1. **UFR: Reasoning Complex** — strongest routed option for constructing an argument, comparing interpretations, identifying assumptions, and synthesizing supplied sources.
2. **Mistral Large Latest** — strong candidate for polished long-form prose, multilingual writing, restructuring, and revision.
3. **UFR: Qwen 3.5 397B / A17B** — promising for extensive synthesis, complex outlines, and technical or multilingual subjects.
4. **GPT 5.6 route** — likely a top option for drafting and revision, although Terra/Luna/Sol cannot be ranked without provider documentation.
5. **UFR: Standard Reasoning** — dependable default for developing thesis, structure, counterarguments, and conclusions.
6. **UFR: Chat Standard** or **Standard Chat** — best for stylistic editing, clarity, transitions, shortening, and adapting tone.
7. **UFR: Vision Complex** — add this when interpreting scientific figures or scanned source material.
8. **nuExtract3** followed by **Numarkdown** — useful preprocessing pipeline for scanned literature: extract the document, normalize it to Markdown, then analyze it with a reasoning model.

### Academic workflow

```mermaid
graph LR
    A[Sources and notes] --> B[nuExtract3 or Numarkdown if needed]
    B --> C[Reasoning Complex: thesis and evidence map]
    C --> D[Mistral Large, Qwen large, or GPT route: draft]
    D --> E[Standard Reasoning: critique logic]
    E --> F[Chat Standard: polish clarity and style]
    F --> G[Human citation and factual verification]
```

Do not ask any model to invent references. Supply the actual papers or bibliographic metadata, require every factual claim to be linked to a supplied source, and manually verify quotations, page numbers, statistics, and citations. AI-generated prose may also need disclosure under your university or journal policy.

## Concise recommendation

- **One model primarily for coding:** **UFR: Coding Complex**; use **Codestral Latest** as the specialist alternative.
- **One model primarily for academic essays:** **UFR: Reasoning Complex** for substance, followed by **Mistral Large Latest** or a verified high-capability GPT 5.6 route for prose polishing.
- **One versatile model for both:** **UFR: Qwen 3.5 397B / A17B** or the strongest documented GPT 5.6 tier.
- **Fast economical option:** **UFR: Coding Fast** for code and **UFR: Chat Fast** or **GLM 5.3 Flash** for prose edits.
- **Avoid starting new durable workflows with:** GLM 5.2, Qwen 3.6 27B, and GPT-5.4 because the labels explicitly say they will be retired or replaced.

# Update models with this python script

1. Copy and paste this python script to a new text file.
2. Adjust the script according to your openwebui account and device. For example, change the location of python according to your python installation environment and place your API string in the OPENWEBUI_TOKEN variable. 
3. Save the text file as a .py extension file, for example, `yourFilename.py`.
4. In unix environment, call the script in terminal `python3 yourFilename.py`

```python
#!/usr/bin/env python3
import copy
import os
from pathlib import Path

import requests
import yaml

OPENWEBUI_URL = "https://openwebui.uni-freiburg.de"
OPENWEBUI_TOKEN = "TYPE-YOUR-API-HERE"
CONFIG_PATH = Path(os.environ.get("CONTINUE_CONFIG_PATH", "~/.continue/config.yaml")).expanduser()


def int_or_none(value):
    try:
        return int(value) if value is not None else None
    except (TypeError, ValueError):
        return None


def fetch_models():
    headers = {
        "Authorization": f"Bearer {OPENWEBUI_TOKEN}",
        "Accept": "application/json",
    }

    resp = requests.get(f"{OPENWEBUI_URL}/api/models", headers=headers, timeout=30)
    resp.raise_for_status()

    ctype = resp.headers.get("content-type", "")
    if "application/json" not in ctype:
        raise RuntimeError(f"Expected JSON, got {ctype}: {resp.text[:300]}")

    payload = resp.json()

    # Handle common response shapes
    if isinstance(payload, list):
        return payload

    if isinstance(payload, dict):
        for key in ("data", "models", "items", "result"):
            if isinstance(payload.get(key), list):
                return payload[key]

    raise RuntimeError(f"Unsupported models response shape: {type(payload)}")


def extract_model_id(model):
    if isinstance(model, str):
        return model
    if not isinstance(model, dict):
        return str(model)

    return (
        model.get("id")
        or model.get("name")
        or model.get("model")
        or model.get("slug")
        or "unknown-model"
    )


def extract_metadata(model):
    """
    Read metadata if the API provides it.
    We look for common key names and also nested `metadata`.
    """
    if not isinstance(model, dict):
        return {}

    # Merge nested metadata into the main dict if present
    merged = dict(model)
    nested = model.get("metadata")
    if isinstance(nested, dict):
        merged.update(nested)

    meta = {}

    # Context length candidates
    for key in (
        "context_length",
        "contextLength",
        "max_context_length",
        "maxContextLength",
        "context_window",
        "contextWindow",
        "max_input_tokens",
        "maxInputTokens",
    ):
        val = int_or_none(merged.get(key))
        if val:
            meta["contextLength"] = val
            break

    # Output token limit candidates
    for key in (
        "max_tokens",
        "maxTokens",
        "max_output_tokens",
        "maxOutputTokens",
        "max_completion_tokens",
        "maxCompletionTokens",
        "completion_tokens",
    ):
        val = int_or_none(merged.get(key))
        if val:
            meta["maxTokens"] = val
            break

    # Only use explicit roles if the API actually provides them
    roles = merged.get("roles")
    if isinstance(roles, list) and all(isinstance(r, str) for r in roles):
        meta["roles"] = roles

    return meta


def find_template(existing_models, model_id):
    """
    Prefer an exact existing config entry for the same model id.
    Otherwise, use the first OpenAI entry as a template.
    """
    if isinstance(existing_models, list):
        for item in existing_models:
            if isinstance(item, dict) and item.get("model") == model_id:
                base = copy.deepcopy(item)
                base.pop("name", None)
                base.pop("model", None)
                return base

        for item in existing_models:
            if isinstance(item, dict) and item.get("provider") == "openai":
                base = copy.deepcopy(item)
                base.pop("name", None)
                base.pop("model", None)
                return base

    return None


def default_template():
    return {
        "provider": "openai",
        "apiBase": f"{OPENWEBUI_URL}/api",
        "apiKey": OPENWEBUI_TOKEN,
        "roles": ["chat", "edit", "apply"],
        "defaultCompletionOptions": {
            "contextLength": 262144,
            "maxTokens": 32768,
        },
    }


def build_entry(model, template):
    mid = extract_model_id(model)
    meta = extract_metadata(model)

    entry = copy.deepcopy(template)
    entry["name"] = model.get("name") if isinstance(model, dict) and model.get("name") else mid
    entry["model"] = mid

    # Preserve template roles unless explicit roles are provided by metadata
    if "roles" in meta:
        entry["roles"] = meta["roles"]

    opts = entry.get("defaultCompletionOptions") or {}
    opts = copy.deepcopy(opts)

    if "contextLength" in meta:
        opts["contextLength"] = meta["contextLength"]

    if "maxTokens" in meta:
        opts["maxTokens"] = meta["maxTokens"]

    entry["defaultCompletionOptions"] = opts
    return entry


def main():
    models = fetch_models()

    if CONFIG_PATH.exists():
        with CONFIG_PATH.open("r") as f:
            cfg = yaml.safe_load(f) or {}
    else:
        cfg = {}

    existing_models = cfg.get("models", [])
    base = find_template(existing_models, None) or default_template()

    new_models = []
    for model in models:
        mid = extract_model_id(model)
        template = find_template(existing_models, mid) or base
        new_models.append(build_entry(model, template))

    cfg["models"] = new_models

    with CONFIG_PATH.open("w") as f:
        yaml.safe_dump(cfg, f, sort_keys=False, allow_unicode=True)

    print(f"Updated {CONFIG_PATH} with {len(new_models)} models.")


if __name__ == "__main__":
    main()
```
