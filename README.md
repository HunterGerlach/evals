# eval

## Pre-reqs:

- Git
- Clone this repo <https://github.com/HunterGerlach/evals>
- Enter the repo (`cd evals`)
- Node/NPM
- PromptFoo (via npm/npx - e.g.: npm install promptfoo@latest)
- Ollama/Ramalama
- Download models (e.g. ollama pull llama2, ollama pull granite3.2)

## Chapter 1 - Simple Evals

1. Install Promptfoo: https://www.promptfoo.dev/docs/installation/

```bash
# option 1
npm install promptfoo@latest

# option 2
npx promptfoo@latest
```

2. Set your OpenAI API key:

```bash
export OPENAI_API_KEY=my-fake-api-key
```

3. Go into chapter 1 directory:

```bash
cd ch1
```

4. Run the evaluation:

```bash
# option 1
promptfoo eval

# option 2
npx promptfoo eval
```

### What's happening?

This example:

- Tests a translation prompt for the llama2 model


## Chapter 2 - Multiple Models

Note: Continue using your promptfooconfig.yaml from chapter 1. Chapter 2 config is only available for reference.

1. Add a second model to the promptfooconfig.yaml: `granite3.2`

2. Eval the models/prompt:

```bash
# option 1
promptfoo eval

# option 2
npx promptfoo eval
```

3. Investigate the results

4. Display the report:

```bash
# option 1
promptfoo view

# option 2
npx promptfoo view
```

Note: `CTRL+C` to end report serving.

### What's happening?

This example:

- Tests a translation prompt for the two models
- Compares outputs between llama2 and granite3.2 models
- Uses two test cases with different languages and inputs
- Displays the results as a report

## Chapter 3 - Prompt Engineering

Note: Continue iterating on your promptfooconfig.yaml from chapter 1. Chapter 3 config is only available for reference.

1. We noticed last time that the model failed one of its evaluations.

2. Iteratively edit the prompt and run evals until all evals pass.

3. Once the evals all pass, display the report:

```bash
# option 1
promptfoo view

# option 2
npx promptfoo view
```

Note: `CTRL+C` to end report serving.

### What's happening?

This example:

- User updates prompt to overcome eval failure
- Tests a translation prompt for the two models
- Compares outputs between llama2 and granite3.2 models
- Uses two test cases with different languages and inputs
- Displays the results as a report

## Assignment

1. Review the types of prompts that can be run with Promptfoo: <https://www.promptfoo.dev/docs/configuration/parameters/>

2. Create new evals and store them in the prompts directory.

3. Submit a PR with your changes to this repo <https://github.com/HunterGerlach/evals>