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

5. Now try running the same command multiple times to simulate multiple (10) users:

```bash
# option 1
promptfoo eval --repeat 10

# option 2
npx promptfoo eval --repeat 10
```

Note: Promptfoo caches requests, so if you make the same CLI call you will get the same response.
To get a new response, simply add `--no-cache` to the end of your calls and it will run a fresh request.

### What's happening?

This example:

- Tests a prompt for the granite3.2 model
- Simulates 10 users prompting with the granite3.2 model

## Chapter 2 - Multiple Models

Note: Continue using your promptfooconfig.yaml from chapter 1. Chapter 2 config is only available for reference.

1. Add a second model to the promptfooconfig.yaml: `llama2`

2. Eval the models/prompt:

```bash
# option 1
promptfoo eval

# option 2
npx promptfoo eval
```

3. Investigate the results

4. See run the same eval, but repeat multiple times to see the results for multiple (10) users:

```bash
# option 1
promptfoo eval --repeat 10

# option 2
npx promptfoo eval --repeat 10
```

5. Display the report:

```bash
# option 1
promptfoo view

# option 2
npx promptfoo view
```

Note: `CTRL+C` to end report serving.

### What's happening?

This example:

- Tests a prompt for the two models
- Compares outputs between llama2 and granite3.2 models
- Uses test case with different inputs for single and multiple users
- Displays the results as a report

## Chapter 3 - Prompt Engineering

Note: Continue iterating on your promptfooconfig.yaml from chapter 1. Chapter 3 config is only available for reference.

1. We noticed last time that the model consistenyl failed one of its evaluations for a certain model.

2. Iteratively edit the prompt and run evals until all evals pass (a majority of the time - remember, this is generative AI and results are non-deterministic!).

3. Once you think you have a successful prompt, repeat multiple times to see the results as simulated for multiple (10) users:

```bash
# option 1
promptfoo eval --repeat 10

# option 2
npx promptfoo eval --repeat 10
```

4. If your results are good enough (~>=75% passing), display the report:

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
- Uses test cases with different inputs
- Verifies results for multiple users
- Displays the results as a report

## Assignment

1. Review the types of prompts that can be run with Promptfoo: <https://www.promptfoo.dev/docs/configuration/parameters/>

2. Create new evals and store them in the prompts directory.

3. Submit a PR with your changes to this repo <https://github.com/HunterGerlach/evals>