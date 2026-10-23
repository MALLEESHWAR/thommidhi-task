# Thommidhi Task 05 — Creator Request Evaluation

## Contents
- `eval_cases.json`: 20 realistic creator requests and expected tool calls.
- `score_transcript.py`: Python heuristic scorer.
- `sample_transcript.txt`: illustrative sample only, **not a real Task 1 transcript**.
- `results_sample.txt`: output from scoring the illustrative sample.

## Run locally
```bash
python score_transcript.py eval_cases.json sample_transcript.txt
```

To evaluate a real Task 1 transcript, save the actual transcript/tool-call log as `task1_transcript.txt`, then run:
```bash
python score_transcript.py eval_cases.json task1_transcript.txt
```

## Tool names are a proposed evaluation contract
The expected tool names (`get_creator_terms`, `analyze_brand_offer`, etc.) are illustrative names because the exact tools exposed by Oli must be copied from the real product/tool logs. Replace the expected names with actual tool names before interpreting coverage.

## Scoring approach
The script checks whether expected tool-name strings occur in the transcript and prints portfolio-style coverage. It also runs two basic safety-pattern heuristics. This is a starter evaluation, not a semantic judge: a matching word in prose can create a false positive, and a real tool call may be missed if its name is different.

## Honest reporting
Do not describe the sample transcript as a real product test. Include actual Task 1 evidence and results before claiming that the real transcript was evaluated.
