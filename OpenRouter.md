Docs
The future will bring us hundreds of language models and dozens of providers for each. How will you choose the best?

Prioritize price or performance. OpenRouter scouts for the lowest prices and best latencies/throughputs across dozens of providers, and lets you choose how to prioritize them.

Standardized API. No need to change your code when switching between models or providers. You can even let users your choose and pay for their own.

The best models will be used the most. Evals are flawed. Instead, compare models by how often they're used, and soon, for which purposes. Chat with multiple at once in the Playground.

Quick Start
typescript
python
shell

Copy
fetch("https://openrouter.ai/api/v1/chat/completions", {
  method: "POST",
  headers: {
    "Authorization": `Bearer ${OPENROUTER_API_KEY}`,
    "HTTP-Referer": `${YOUR_SITE_URL}`, // Optional, for including your app on openrouter.ai rankings.
    "X-Title": `${YOUR_SITE_NAME}`, // Optional. Shows in rankings on openrouter.ai.
    "Content-Type": "application/json"
  },
  body: JSON.stringify({
    "model": "openai/gpt-3.5-turbo",
    "messages": [
      {"role": "user", "content": "What is the meaning of life?"},
    ],
  })
});
You can also use OpenRouter with OpenAI's client API:

typescript
python

Copy
import OpenAI from "openai"

const openai = new OpenAI({
  baseURL: "https://openrouter.ai/api/v1",
  apiKey: $OPENROUTER_API_KEY,
  defaultHeaders: {
    "HTTP-Referer": $YOUR_SITE_URL, // Optional, for including your app on openrouter.ai rankings.
    "X-Title": $YOUR_SITE_NAME, // Optional. Shows in rankings on openrouter.ai.
  },
  // dangerouslyAllowBrowser: true,
})
async function main() {
  const completion = await openai.chat.completions.create({
    model: "openai/gpt-3.5-turbo",
    messages: [
      { role: "user", content: "Say this is a test" }
    ],
  })

  console.log(completion.choices[0].message)
}
main()
Supported Models
Model usage can be paid by users, developers, or both, and may shift in availability. You can also fetch models, prices, and limits via API. 
If you'd like to add an open source model directly to OpenRouter, visit our Github here.

Text models
Show tokens per $

Model Name
& ID	Prompt cost
($ per 1k tokens)	Completion cost
($ per 1k tokens)	Context
(tokens)	Moderation
Lynn: Llama 3 Soliloquy 8B
lynn/soliloquy-l3	
$0
100% off
$0
100% off
24,576
None
Nous: Capybara 7B (free)
nousresearch/nous-capybara-7b:free	
$0
100% off
$0
100% off
4,096
None
Mistral 7B Instruct (free)
mistralai/mistral-7b-instruct:free	
$0
100% off
$0
100% off
32,768
None
OpenChat 3.5 (free)
openchat/openchat-7b:free	
$0
100% off
$0
100% off
8,192
None
MythoMist 7B (free)
gryphe/mythomist-7b:free	
$0
100% off
$0
100% off
32,768
None
Toppy M 7B (free)
undi95/toppy-m-7b:free	
$0
100% off
$0
100% off
4,096
None
Cinematika 7B (alpha) (free)
openrouter/cinematika-7b:free	
$0
100% off
$0
100% off
8,000
None
Google: Gemma 7B (free)
google/gemma-7b-it:free	
$0
100% off
$0
100% off
8,192
None
Psyfighter 13B
jebcarter/psyfighter-13b	
$0.001
90% off
$0.001
90% off
4,096
None
Psyfighter v2 13B
koboldai/psyfighter-13b-2	
$0.001
90% off
$0.001
90% off
4,096
None
Neural Chat 7B v3.1
intel/neural-chat-7b	
$0.005
50% off
$0.005
50% off
4,096
None
Llava 13B
haotian-liu/llava-13b	
$0.005
50% off
$0.005
50% off
2,048
None
Nous: Hermes 2 Vision 7B (alpha)
nousresearch/nous-hermes-2-vision-7b	
$0.005
50% off
$0.005
50% off
4,096
None
MythoMax 13B
gryphe/mythomax-l2-13b	
$0.00018
40% off
$0.00018
40% off
4,096
None
MythoMax 13B (extended)
gryphe/mythomax-l2-13b:extended	
$0.00018
40% off
$0.00018
40% off
8,192
None
Meta: Llama v2 13B Chat
meta-llama/llama-2-13b-chat	
$0.0001206
33% off
$0.0001206
33% off
4,096
None
Pygmalion: Mythalion 13B
pygmalionai/mythalion-13b	
$0.001125
25% off
$0.001125
25% off
8,192
None
Xwin 70B
xwin-lm/xwin-lm-70b	
$0.00375
25% off
$0.00375
25% off
8,192
None
Goliath 120B
alpindale/goliath-120b	
$0.009375
25% off
$0.009375
25% off
6,144
None
Noromaid 20B
neversleep/noromaid-20b	
$0.00225
25% off
$0.00225
25% off
8,192
None
MythoMist 7B
gryphe/mythomist-7b	
$0.000375
25% off
$0.000375
25% off
32,768
None
Midnight Rose 70B
sophosympatheia/midnight-rose-70b	
$0.009
25% off
$0.009
25% off
4,096
None
Fimbulvetr 11B v2
sao10k/fimbulvetr-11b-v2	
$0.0005499
25% off
$0.002826
25% off
8,192
None
ReMM SLERP 13B (extended)
undi95/remm-slerp-l2-13b:extended	
$0.001125
25% off
$0.001125
25% off
6,144
None
Meta: Llama 3 8B Instruct (extended)
meta-llama/llama-3-8b-instruct:extended	
$0.0002751
25% off
$0.0003249
25% off
16,384
None
Mancer: Weaver (alpha)
mancer/weaver	
$0.003375
25% off
$0.003375
25% off
8,000
None
Nous: Hermes 13B
nousresearch/nous-hermes-llama2-13b	
$0.00027
10% off
$0.00027
10% off
4,096
None
Nous: Capybara 7B
nousresearch/nous-capybara-7b	
$0.00018
10% off
$0.00018
10% off
4,096
None
Meta: CodeLlama 34B Instruct
meta-llama/codellama-34b-instruct	
$0.00072
10% off
$0.00072
10% off
8,192
None
Meta: CodeLlama 70B Instruct
codellama/codellama-70b-instruct	
$0.00081
10% off
$0.00081
10% off
2,048
None
Phind: CodeLlama 34B v2
phind/phind-codellama-34b	
$0.00072
10% off
$0.00072
10% off
4,096
None
OpenHermes 2 Mistral 7B
teknium/openhermes-2-mistral-7b	
$0.00018
10% off
$0.00018
10% off
4,096
None
OpenHermes 2.5 Mistral 7B
teknium/openhermes-2.5-mistral-7b	
$0.00018
10% off
$0.00018
10% off
4,096
None
ReMM SLERP 13B
undi95/remm-slerp-l2-13b	
$0.00027
10% off
$0.00027
10% off
4,096
None
Cinematika 7B (alpha)
openrouter/cinematika-7b	
$0.00018
10% off
$0.00018
10% off
8,000
None
Yi 34B Chat
01-ai/yi-34b-chat	
$0.00072
10% off
$0.00072
10% off
4,096
None
Yi 34B (base)
01-ai/yi-34b	
$0.00072
10% off
$0.00072
10% off
4,096
None
Yi 6B (base)
01-ai/yi-6b	
$0.000126
10% off
$0.000126
10% off
4,096
None
StripedHyena Nous 7B
togethercomputer/stripedhyena-nous-7b	
$0.00018
10% off
$0.00018
10% off
32,768
None
StripedHyena Hessian 7B (base)
togethercomputer/stripedhyena-hessian-7b	
$0.00018
10% off
$0.00018
10% off
32,768
None
Mixtral 8x7B (base)
mistralai/mixtral-8x7b	
$0.00054
10% off
$0.00054
10% off
32,768
None
Nous: Hermes 2 Yi 34B
nousresearch/nous-hermes-yi-34b	
$0.00072
10% off
$0.00072
10% off
4,096
None
Nous: Hermes 2 Mixtral 8x7B SFT
nousresearch/nous-hermes-2-mixtral-8x7b-sft	
$0.00054
10% off
$0.00054
10% off
32,000
None
Nous: Hermes 2 Mistral 7B DPO
nousresearch/nous-hermes-2-mistral-7b-dpo	
$0.00018
10% off
$0.00018
10% off
8,192
None
Mistral OpenOrca 7B
open-orca/mistral-7b-openorca	
$0.0001425
5% off
$0.0001425
5% off
8,192
None
Hugging Face: Zephyr 7B
huggingfaceh4/zephyr-7b-beta	
$0.0001425
5% off
$0.0001425
5% off
4,096
None
OpenAI: GPT-3.5 Turbo
openai/gpt-3.5-turbo	
$0.0005
$0.0015
16,385
Moderated
OpenAI: GPT-3.5 Turbo 16k
openai/gpt-3.5-turbo-0125	
$0.0005
$0.0015
16,385
Moderated
OpenAI: GPT-3.5 Turbo 16k
openai/gpt-3.5-turbo-16k	
$0.003
$0.004
16,385
Moderated
OpenAI: GPT-4 Turbo
openai/gpt-4-turbo	
$0.01
$0.03
128,000
Moderated
OpenAI: GPT-4 Turbo Preview
openai/gpt-4-turbo-preview	
$0.01
$0.03
128,000
Moderated
OpenAI: GPT-4
openai/gpt-4	
$0.03
$0.06
8,191
Moderated
OpenAI: GPT-4 32k
openai/gpt-4-32k	
$0.06
$0.12
32,767
Moderated
OpenAI: GPT-4 Vision
openai/gpt-4-vision-preview	
$0.01
$0.03
128,000
Moderated
OpenAI: GPT-3.5 Turbo Instruct
openai/gpt-3.5-turbo-instruct	
$0.0015
$0.002
4,095
Moderated
Google: PaLM 2 Chat
google/palm-2-chat-bison	
$0.00025
$0.0005
25,804
None
Google: PaLM 2 Code Chat
google/palm-2-codechat-bison	
$0.00025
$0.0005
20,070
None
Google: PaLM 2 Chat 32k
google/palm-2-chat-bison-32k	
$0.00025
$0.0005
91,750
None
Google: PaLM 2 Code Chat 32k
google/palm-2-codechat-bison-32k	
$0.00025
$0.0005
91,750
None
Google: Gemini Pro 1.0
google/gemini-pro	
$0.000125
$0.000375
91,728
None
Google: Gemini Pro Vision 1.0
google/gemini-pro-vision	
$0.000125
$0.000375
45,875
None
Google: Gemini Pro 1.5 (preview)
google/gemini-pro-1.5	
$0.0025
$0.0075
2,800,000
None
Perplexity: PPLX 70B Online
perplexity/pplx-70b-online	
$0.001
$0.001
4,096
None
Perplexity: PPLX 7B Online
perplexity/pplx-7b-online	
$0.0002
$0.0002
4,096
None
Perplexity: PPLX 7B Chat
perplexity/pplx-7b-chat	
$0.0002
$0.0002
8,192
None
Perplexity: PPLX 70B Chat
perplexity/pplx-70b-chat	
$0.001
$0.001
4,096
None
Perplexity: Sonar 7B
perplexity/sonar-small-chat	
$0.0002
$0.0002
16,384
None
Perplexity: Sonar 8x7B
perplexity/sonar-medium-chat	
$0.0006
$0.0006
16,384
None
Perplexity: Sonar 7B Online
perplexity/sonar-small-online	
$0.0002
$0.0002
12,000
None
Perplexity: Sonar 8x7B Online
perplexity/sonar-medium-online	
$0.0006
$0.0006
12,000
None
Anthropic: Claude 3 Opus
anthropic/claude-3-opus	
$0.015
$0.075
200,000
Moderated
Anthropic: Claude 3 Sonnet
anthropic/claude-3-sonnet	
$0.003
$0.015
200,000
Moderated
Anthropic: Claude 3 Haiku
anthropic/claude-3-haiku	
$0.00025
$0.00125
200,000
Moderated
Anthropic: Claude 3 Opus (self-moderated)
anthropic/claude-3-opus:beta	
$0.015
$0.075
200,000
None
Anthropic: Claude 3 Sonnet (self-moderated)
anthropic/claude-3-sonnet:beta	
$0.003
$0.015
200,000
None
Anthropic: Claude 3 Haiku (self-moderated)
anthropic/claude-3-haiku:beta	
$0.00025
$0.00125
200,000
None
Meta: Llama v2 70B Chat
meta-llama/llama-2-70b-chat	
$0.0006
$0.0019
4,096
None
Nous: Capybara 34B
nousresearch/nous-capybara-34b	
$0.0009
$0.0009
32,768
None
Airoboros 70B
jondurbin/airoboros-l2-70b	
$0.0007
$0.0009
4,096
None
Bagel 34B v0.2
jondurbin/bagel-34b	
$0.00575
$0.00575
8,000
None
Chronos Hermes 13B v2
austism/chronos-hermes-13b	
$0.00018
$0.00018
4,096
None
Mistral 7B Instruct
mistralai/mistral-7b-instruct	
$0.0001
$0.00025
32,768
None
OpenChat 3.5
openchat/openchat-7b	
$0.00013
$0.00013
8,192
None
Toppy M 7B
undi95/toppy-m-7b	
$0.00015
$0.00015
4,096
None
lzlv 70B
lizpreciatior/lzlv-70b-fp16-hf	
$0.0007
$0.0008
4,096
None
Mixtral 8x7B Instruct
mistralai/mixtral-8x7b-instruct	
$0.00024
$0.00024
32,768
None
Dolphin 2.6 Mixtral 8x7B 🐬
cognitivecomputations/dolphin-mixtral-8x7b	
$0.0005
$0.0005
32,000
None
Noromaid Mixtral 8x7B Instruct
neversleep/noromaid-mixtral-8x7b-instruct	
$0.008
$0.008
8,000
None
Nous: Hermes 2 Mixtral 8x7B DPO
nousresearch/nous-hermes-2-mixtral-8x7b-dpo	
$0.0003
$0.0005
32,000
None
RWKV v5 World 3B
rwkv/rwkv-5-world-3b	
$0
$0
10,000
None
RWKV v5 3B AI Town
recursal/rwkv-5-3b-ai-town	
$0
$0
10,000
None
RWKV v5: Eagle 7B
recursal/eagle-7b	
$0
$0
10,000
None
Google: Gemma 7B
google/gemma-7b-it	
$0.0001
$0.0001
8,192
None
Databricks: DBRX 132B Instruct
databricks/dbrx-instruct	
$0.0006
$0.0006
32,768
None
Zephyr 141B-A35B
huggingfaceh4/zephyr-orpo-141b-a35b	
$0.00065
$0.00065
65,536
None
Meta: Llama 3 8B Instruct
meta-llama/llama-3-8b-instruct	
$0.0001
$0.0001
8,192
None
Meta: Llama 3 70B Instruct
meta-llama/llama-3-70b-instruct	
$0.0008
$0.0008
8,192
None
WizardLM-2 8x22B
microsoft/wizardlm-2-8x22b	
$0.00065
$0.00065
65,536
None
WizardLM-2 7B
microsoft/wizardlm-2-7b	
$0.0001
$0.0001
32,000
None
Mistral: Mixtral 8x22B (base)
mistralai/mixtral-8x22b	
$0.0009
$0.0009
65,536
None
Mistral: Mixtral 8x22B Instruct
mistralai/mixtral-8x22b-instruct	
$0.00065
$0.00065
65,536
None
Anthropic: Claude v2
anthropic/claude-2	
$0.008
$0.024
200,000
Moderated
Anthropic: Claude v2.1
anthropic/claude-2.1	
$0.008
$0.024
200,000
Moderated
Anthropic: Claude v2.0
anthropic/claude-2.0	
$0.008
$0.024
100,000
Moderated
Anthropic: Claude Instant v1
anthropic/claude-instant-1	
$0.0008
$0.0024
100,000
Moderated
Anthropic: Claude Instant v1.2
anthropic/claude-instant-1.2	
$0.0008
$0.0024
100,000
Moderated
Anthropic: Claude v2 (self-moderated)
anthropic/claude-2:beta	
$0.008
$0.024
200,000
None
Anthropic: Claude v2.1 (self-moderated)
anthropic/claude-2.1:beta	
$0.008
$0.024
200,000
None
Anthropic: Claude v2.0 (self-moderated)
anthropic/claude-2.0:beta	
$0.008
$0.024
100,000
None
Anthropic: Claude Instant v1 (self-moderated)
anthropic/claude-instant-1:beta	
$0.0008
$0.0024
100,000
None
Hugging Face: Zephyr 7B (free)
huggingfaceh4/zephyr-7b-beta:free	
$0
$0
4,096
None
Mixtral 8x7B Instruct (nitro)
mistralai/mixtral-8x7b-instruct:nitro	
$0.0005
$0.0005
32,768
None
Meta: Llama v2 70B Chat (nitro)
meta-llama/llama-2-70b-chat:nitro	
$0.0009
$0.0009
4,096
None
MythoMax 13B (nitro)
gryphe/mythomax-l2-13b:nitro	
$0.0002
$0.0002
4,096
None
Mistral 7B Instruct (nitro)
mistralai/mistral-7b-instruct:nitro	
$0.0002
$0.0002
32,768
None
Google: Gemma 7B (nitro)
google/gemma-7b-it:nitro	
$0.0002
$0.0002
8,192
None
Toppy M 7B (nitro)
undi95/toppy-m-7b:nitro	
$0.00015
$0.00015
4,096
None
WizardLM-2 8x22B (nitro)
microsoft/wizardlm-2-8x22b:nitro	
$0.001
$0.001
65,536
None
Meta: Llama 3 8B Instruct (nitro)
meta-llama/llama-3-8b-instruct:nitro	
$0.0002
$0.0002
8,192
None
Meta: Llama 3 70B Instruct (nitro)
meta-llama/llama-3-70b-instruct:nitro	
$0.0009
$0.0009
8,192
None
Mistral Tiny
mistralai/mistral-tiny	
$0.00025
$0.00025
32,000
None
Mistral Small
mistralai/mistral-small	
$0.002
$0.006
32,000
None
Mistral Medium
mistralai/mistral-medium	
$0.0027
$0.0081
32,000
None
Mistral Large
mistralai/mistral-large	
$0.008
$0.024
32,000
None
Cohere: Command
cohere/command	
$0.001
$0.002
4,096
None
Cohere: Command R
cohere/command-r	
$0.0005
$0.0015
128,000
None
Cohere: Command R+
cohere/command-r-plus	
$0.003
$0.015
128,000
None

Older versions
Media models
OpenAI: Shap-e
openai/shap-e
$0.01 / 32 steps
Note: Different models tokenize text in different ways. Some models break up text into chunks of multiple characters (GPT, Claude, Llama, etc) while others tokenize by character (PaLM). This means that the number of tokens may vary depending on the model.

Provider Routing
OpenRouter routes each request to the best available model provider for your preferences. You can customize them using the provider object in the request body. Here are the available options:

Custom Provider Selection
You can set the providers that OpenRouter will use for your request using the order field. The router will filter this list to only include providers that are available for the model you're using, and then try one at a time, failing if none are available. If you don't set this field, the router will use the default ordering shown on the model page.

typescript

Copy
fetch("https://openrouter.ai/api/v1/chat/completions", {
  method: "POST",
  headers: {
    "Authorization": `Bearer ${OPENROUTER_API_KEY}`,
    "HTTP-Referer": `${YOUR_SITE_URL}`, // Optional, for including your app on openrouter.ai rankings.
    "X-Title": `${YOUR_SITE_NAME}`, // Optional. Shows in rankings on openrouter.ai.
    "Content-Type": "application/json"
  },
  body: JSON.stringify({
    "model": "mistralai/mixtral-8x7b-instruct",
    "messages": [
      {"role": "user", "content": "Hello"},
    ],
    "provider": {
      "order": [
        "Azure",
        "Together"
      ]
    },
  })
});
Required Parameters (beta)
By default, providers that don't support a given LLM parameter will ignore them. But you can change this and only filter for providers that support the parameters in your request.

For example, to only use providers that support JSON formatting:

typescript

Copy
fetch("https://openrouter.ai/api/v1/chat/completions", {
  method: "POST",
  headers: {
    "Authorization": `Bearer ${OPENROUTER_API_KEY}`,
    "HTTP-Referer": `${YOUR_SITE_URL}`, // Optional, for including your app on openrouter.ai rankings.
    "X-Title": `${YOUR_SITE_NAME}`, // Optional. Shows in rankings on openrouter.ai.
    "Content-Type": "application/json"
  },
  body: JSON.stringify({
    "model": "mistralai/mixtral-8x7b-instruct",
    "messages": [
      {"role": "user", "content": "Hello"},
    ],
    "provider": {
      "require_parameters": true
    },
    "response_format": {
      "type": "json_object"
    },
  })
});
Data Privacy
Some model providers may log prompts, so we display them with a Data Policy tag on model pages. This is not a definitive source of third party data policies, but represents our best knowledge.

OpenRouter's data policy is managed on your Account page. You can disable logging there to also disable third party model providers that store logs for purposes like training. Alternatively, you can skip them on a per-request basis:

typescript

Copy
fetch("https://openrouter.ai/api/v1/chat/completions", {
  method: "POST",
  headers: {
    "Authorization": `Bearer ${OPENROUTER_API_KEY}`,
    "HTTP-Referer": `${YOUR_SITE_URL}`, // Optional, for including your app on openrouter.ai rankings.
    "X-Title": `${YOUR_SITE_NAME}`, // Optional. Shows in rankings on openrouter.ai.
    "Content-Type": "application/json"
  },
  body: JSON.stringify({
    "model": "mistralai/mixtral-8x7b-instruct",
    "messages": [
      {"role": "user", "content": "Hello"},
    ],
    "provider": {
      "data_collection": "deny"
    },
  })
});
Disabling a provider causes the router to skip over it and proceed to the next best one.

Disabling Fallbacks
To guarantee that your request is only served by the top (lowest-cost) provider, you can disable fallbacks:

typescript

Copy
fetch("https://openrouter.ai/api/v1/chat/completions", {
  method: "POST",
  headers: {
    "Authorization": `Bearer ${OPENROUTER_API_KEY}`,
    "HTTP-Referer": `${YOUR_SITE_URL}`, // Optional, for including your app on openrouter.ai rankings.
    "X-Title": `${YOUR_SITE_NAME}`, // Optional. Shows in rankings on openrouter.ai.
    "Content-Type": "application/json"
  },
  body: JSON.stringify({
    "model": "mistralai/mixtral-8x7b-instruct",
    "messages": [
      {"role": "user", "content": "Hello"},
    ],
    "provider": {
      "allow_fallbacks": false
    },
  })
});
For a complete list of options, see this JSON schema:

javascript

Copy
{
  "$ref": "#/definitions/ProviderPreferences",
  "definitions": {
    "ProviderPreferences": {
      "type": "object",
      "properties": {
        "allow_fallbacks": {
          "type": "boolean",
          "description": "Whether to allow backup providers to serve requests
- true: (default) when the primary provider is unavailable, use the next best provider.
- false: use only the primary provider, and return the upstream error if it's unavailable.
",
          "default": true
        },
        "require_parameters": {
          "type": "boolean",
          "description": "Whether to filter providers to only those that support the parameters you've provided. If this setting is omitted or set to false, then providers will receive only the parameters they support, and ignore the rest.",
          "default": false
        },
        "data_collection": {
          "type": "string",
          "enum": [
            "deny",
            "allow"
          ],
          "description": "Data collection setting. If no available model provider meets the requirement, your request will return an error.
- allow: (default) allow providers which store user data non-transiently and may train on it
- deny: use only providers which do not collect user data.
",
          "default": "allow"
        },
        "order": {
          "type": "array",
          "items": {
            "type": "string",
            "enum": [
              "OpenAI",
              "Anthropic",
              "HuggingFace",
              "Google",
              "Mancer",
              "Mancer 2",
              "Together",
              "DeepInfra",
              "Azure",
              "Modal",
              "AnyScale",
              "Replicate",
              "Perplexity",
              "Recursal",
              "Fireworks",
              "Mistral",
              "Groq",
              "Cohere",
              "Lepton",
              "OctoAI",
              "Novita",
              "Lynn"
            ]
          },
          "description": "An ordered list of provider names. The router will attempt to use the first provider in the subset of this list that supports your requested model, and fall back to the next if it is unavailable. If no providers are available, the request will fail with an error message."
        }
      },
      "additionalProperties": false
    }
  },
  "$schema": "http://json-schema.org/draft-07/schema#"
}
Model Routing
Multi-model routing is under development 👀

In the meantime, OpenRouter provides two options:

The Auto router, a special model ID that you can use to choose between selected high-quality models based on heuristics applied to your prompt.

The models array, which lets you automatically try other models if the primary model's providers are down, rate-limited, or refuse to reply due to content moderation required by all providers:

json

{
  "models": ["anthropic/claude-2.1", "gryphe/mythomax-l2-13b"],
  "route": "fallback",
  ... // Other params
}
If the model you selected returns an error, OpenRouter will try to use the fallback model instead. If the fallback model is down or returns an error, OpenRouter will return that error.

By default, any error can trigger the use of a fallback model, including context length validation errors, moderation flags for filtered models, rate-limiting, and downtime.

Requests are priced using the model that was used, which will be returned in the model attribute of the response body.

If no fallback model is specified but route: "fallback" is still included, OpenRouter will try the most appropriate open-source model available, with pricing less than the primary model (or very close to it).

OAuth PKCE
Users can connect to OpenRouter in one click using Proof Key for Code Exchange (PKCE). Here's an example, and here's a step-by-step:

Send your user to https://openrouter.ai/auth?callback_url=YOUR_SITE_URL

You can optionally include a code_challenge (random password up to 256 digits) for extra security.
For maximum security, we recommend also setting code_challenge_method to S256, and then setting code_challenge to the base64 encoding of the sha256 hash of code_verifier, which you will submit in Step 2. More info in Auth0's docs.
Once logged in, they'll be redirected back to your site with a code in the URL. Make an API call (can be frontend or backend) to exchange the code for a user-controlled API key. And that's it for PKCE!

Look for the code query parameter, e.g. ?code=....
typescript

fetch("https://openrouter.ai/api/v1/auth/keys", {
  method: 'POST',
  body: JSON.stringify({
    code: $CODE_FROM_QUERY_PARAM,
    code_verifier: $CODE_VERIFIER // Only needed if you sent a code_challenge in Step 1
  })
});
A fresh API key will be in the result under "key". Store it securely and make OpenAI-style requests (supports streaming as well):
typescript

Copy
fetch("https://openrouter.ai/api/v1/chat/completions", {
  method: "POST",
  headers: {
    "Authorization": `Bearer ${OPENROUTER_API_KEY}`,
    "HTTP-Referer": `${YOUR_SITE_URL}`, // Optional, for including your app on openrouter.ai rankings.
    "X-Title": `${YOUR_SITE_NAME}`, // Optional. Shows in rankings on openrouter.ai.
    "Content-Type": "application/json"
  },
  body: JSON.stringify({
    "model": "anthropic/claude-2",
    "messages": [
      {"role": "system", "content": "You are a helpful assistant."},
      {"role": "user", "content": "Hello!"},
    ],
  })
});
You can use JavaScript or any server-side framework, like Streamlit. The linked example shows multiple models and file Q&A.

API Keys
Users or developers can cover model costs with normal API keys. This allows you to use curl or the OpenAI SDK directly with OpenRouter. Just create an API key, set the api_base, and optionally set a referrer header to make your app discoverable to others on OpenRouter.

Note: API keys on OpenRouter are more powerful than keys used directly for model APIs. They allow users to set credit limits for apps, and they can be used in OAuth flows.

Example code:

python
typescript
shell

Copy
import openai

openai.api_base = "https://openrouter.ai/api/v1"
openai.api_key = $OPENROUTER_API_KEY

response = openai.ChatCompletion.create(
  model="openai/gpt-3.5-turbo",
  messages=[...],
  headers={
    "HTTP-Referer": $YOUR_SITE_URL, # Optional, for including your app on openrouter.ai rankings.
    "X-Title": $YOUR_APP_NAME, # Optional. Shows in rankings on openrouter.ai.
  },
)

reply = response.choices[0].message
To stream with Python, see this example from OpenAI.

Requests
OpenRouter's request and response schemas are very similar to the OpenAI Chat API, with a few small differences. At a high level, OpenRouter normalizes the schema across models and providers so you only need to learn one.

Request Body
Here's the request schema as a TypeScript type. This will be the body of your POST request to the /api/v1/chat/completions endpoint (see the quick start above for an example).

typescript

// Definitions of subtypes are below
type Request = {
  // Either "messages" or "prompt" is required
  messages?: Message[];
  prompt?: string;

  // If "model" is unspecified, uses the user's default
  model?: string; // See "Supported Models" section

  // Allows to force the model to produce specific output format.
  // Only supported by OpenAI models, Nitro models, and some others - check the
  // providers on the model page on openrouter.ai/models to see if it's supported,
  // and set `require_parameters` to true in your Provider Preferences. See
  // openrouter.ai/docs#provider-routing
  response_format?: { type: 'json_object' };

  stop?: string | string[];
  stream?: boolean; // Enable streaming

  // See LLM Parameters (openrouter.ai/docs#parameters)
  max_tokens?: number; // Range: [1, context_length)
  temperature?: number; // Range: [0, 2]
  top_p?: number; // Range: (0, 1]
  top_k?: number; // Range: [1, Infinity) Not available for OpenAI models
  frequency_penalty?: number; // Range: [-2, 2]
  presence_penalty?: number; // Range: [-2, 2]
  repetition_penalty?: number; // Range: (0, 2]
  seed?: number; // OpenAI only

  // Function-calling
  // Only natively suported by OpenAI models. For others, we submit
  // a YAML-formatted string with these tools at the end of the prompt.
  tools?: Tool[];
  tool_choice?: ToolChoice;

  // Additional optional parameters
  logit_bias?: { [key: number]: number };

  // OpenRouter-only parameters
  // See "Prompt Transforms" section: openrouter.ai/docs#transforms
  transforms?: string[];
  // See "Model Routing" section: openrouter.ai/docs#model-routing
  models?: string[];
  route?: 'fallback';
  // See "Provider Routing" section: openrouter.ai/docs#provider-routing
  provider?: ProviderPreferences;
};

// Subtypes:

type TextContent = {
  type: 'text';
  text: string;
};

type ImageContentPart = {
  type: 'image_url';
  image_url: {
    url: string; // URL or base64 encoded image data
    detail?: string; // Optional, defaults to 'auto'
  };
Docs
The future will bring us hundreds of language models and dozens of providers for each. How will you choose the best?

Prioritize price or performance. OpenRouter scouts for the lowest prices and best latencies/throughputs across dozens of providers, and lets you choose how to prioritize them.

Standardized API. No need to change your code when switching between models or providers. You can even let users your choose and pay for their own.

The best models will be used the most. Evals are flawed. Instead, compare models by how often they're used, and soon, for which purposes. Chat with multiple at once in the Playground.

Quick Start
typescript
python
shell

Copy
fetch("https://openrouter.ai/api/v1/chat/completions", {
  method: "POST",
  headers: {
    "Authorization": `Bearer ${OPENROUTER_API_KEY}`,
    "HTTP-Referer": `${YOUR_SITE_URL}`, // Optional, for including your app on openrouter.ai rankings.
    "X-Title": `${YOUR_SITE_NAME}`, // Optional. Shows in rankings on openrouter.ai.
    "Content-Type": "application/json"
  },
  body: JSON.stringify({
    "model": "openai/gpt-3.5-turbo",
    "messages": [
      {"role": "user", "content": "What is the meaning of life?"},
    ],
  })
});
You can also use OpenRouter with OpenAI's client API:

typescript
python

Copy
import OpenAI from "openai"

const openai = new OpenAI({
  baseURL: "https://openrouter.ai/api/v1",
  apiKey: $OPENROUTER_API_KEY,
  defaultHeaders: {
    "HTTP-Referer": $YOUR_SITE_URL, // Optional, for including your app on openrouter.ai rankings.
    "X-Title": $YOUR_SITE_NAME, // Optional. Shows in rankings on openrouter.ai.
  },
  // dangerouslyAllowBrowser: true,
})
async function main() {
  const completion = await openai.chat.completions.create({
    model: "openai/gpt-3.5-turbo",
    messages: [
      { role: "user", content: "Say this is a test" }
    ],
  })

  console.log(completion.choices[0].message)
}
main()
Supported Models
Model usage can be paid by users, developers, or both, and may shift in availability. You can also fetch models, prices, and limits via API. 
If you'd like to add an open source model directly to OpenRouter, visit our Github here.

Text models
Show tokens per $

Model Name
& ID	Prompt cost
($ per 1k tokens)	Completion cost
($ per 1k tokens)	Context
(tokens)	Moderation
Lynn: Llama 3 Soliloquy 8B
lynn/soliloquy-l3	
$0
100% off
$0
100% off
24,576
None
Nous: Capybara 7B (free)
nousresearch/nous-capybara-7b:free	
$0
100% off
$0
100% off
4,096
None
Mistral 7B Instruct (free)
mistralai/mistral-7b-instruct:free	
$0
100% off
$0
100% off
32,768
None
OpenChat 3.5 (free)
openchat/openchat-7b:free	
$0
100% off
$0
100% off
8,192
None
MythoMist 7B (free)
gryphe/mythomist-7b:free	
$0
100% off
$0
100% off
32,768
None
Toppy M 7B (free)
undi95/toppy-m-7b:free	
$0
100% off
$0
100% off
4,096
None
Cinematika 7B (alpha) (free)
openrouter/cinematika-7b:free	
$0
100% off
$0
100% off
8,000
None
Google: Gemma 7B (free)
google/gemma-7b-it:free	
$0
100% off
$0
100% off
8,192
None
Psyfighter 13B
jebcarter/psyfighter-13b	
$0.001
90% off
$0.001
90% off
4,096
None
Psyfighter v2 13B
koboldai/psyfighter-13b-2	
$0.001
90% off
$0.001
90% off
4,096
None
Neural Chat 7B v3.1
intel/neural-chat-7b	
$0.005
50% off
$0.005
50% off
4,096
None
Llava 13B
haotian-liu/llava-13b	
$0.005
50% off
$0.005
50% off
2,048
None
Nous: Hermes 2 Vision 7B (alpha)
nousresearch/nous-hermes-2-vision-7b	
$0.005
50% off
$0.005
50% off
4,096
None
MythoMax 13B
gryphe/mythomax-l2-13b	
$0.00018
40% off
$0.00018
40% off
4,096
None
MythoMax 13B (extended)
gryphe/mythomax-l2-13b:extended	
$0.00018
40% off
$0.00018
40% off
8,192
None
Meta: Llama v2 13B Chat
meta-llama/llama-2-13b-chat	
$0.0001206
33% off
$0.0001206
33% off
4,096
None
Pygmalion: Mythalion 13B
pygmalionai/mythalion-13b	
$0.001125
25% off
$0.001125
25% off
8,192
None
Xwin 70B
xwin-lm/xwin-lm-70b	
$0.00375
25% off
$0.00375
25% off
8,192
None
Goliath 120B
alpindale/goliath-120b	
$0.009375
25% off
$0.009375
25% off
6,144
None
Noromaid 20B
neversleep/noromaid-20b	
$0.00225
25% off
$0.00225
25% off
8,192
None
MythoMist 7B
gryphe/mythomist-7b	
$0.000375
25% off
$0.000375
25% off
32,768
None
Midnight Rose 70B
sophosympatheia/midnight-rose-70b	
$0.009
25% off
$0.009
25% off
4,096
None
Fimbulvetr 11B v2
sao10k/fimbulvetr-11b-v2	
$0.0005499
25% off
$0.002826
25% off
8,192
None
ReMM SLERP 13B (extended)
undi95/remm-slerp-l2-13b:extended	
$0.001125
25% off
$0.001125
25% off
6,144
None
Meta: Llama 3 8B Instruct (extended)
meta-llama/llama-3-8b-instruct:extended	
$0.0002751
25% off
$0.0003249
25% off
16,384
None
Mancer: Weaver (alpha)
mancer/weaver	
$0.003375
25% off
$0.003375
25% off
8,000
None
Nous: Hermes 13B
nousresearch/nous-hermes-llama2-13b	
$0.00027
10% off
$0.00027
10% off
4,096
None
Nous: Capybara 7B
nousresearch/nous-capybara-7b	
$0.00018
10% off
$0.00018
10% off
4,096
None
Meta: CodeLlama 34B Instruct
meta-llama/codellama-34b-instruct	
$0.00072
10% off
$0.00072
10% off
8,192
None
Meta: CodeLlama 70B Instruct
codellama/codellama-70b-instruct	
$0.00081
10% off
$0.00081
10% off
2,048
None
Phind: CodeLlama 34B v2
phind/phind-codellama-34b	
$0.00072
10% off
$0.00072
10% off
4,096
None
OpenHermes 2 Mistral 7B
teknium/openhermes-2-mistral-7b	
$0.00018
10% off
$0.00018
10% off
4,096
None
OpenHermes 2.5 Mistral 7B
teknium/openhermes-2.5-mistral-7b	
$0.00018
10% off
$0.00018
10% off
4,096
None
ReMM SLERP 13B
undi95/remm-slerp-l2-13b	
$0.00027
10% off
$0.00027
10% off
4,096
None
Cinematika 7B (alpha)
openrouter/cinematika-7b	
$0.00018
10% off
$0.00018
10% off
8,000
None
Yi 34B Chat
01-ai/yi-34b-chat	
$0.00072
10% off
$0.00072
10% off
4,096
None
Yi 34B (base)
01-ai/yi-34b	
$0.00072
10% off
$0.00072
10% off
4,096
None
Yi 6B (base)
01-ai/yi-6b	
$0.000126
10% off
$0.000126
10% off
4,096
None
StripedHyena Nous 7B
togethercomputer/stripedhyena-nous-7b	
$0.00018
10% off
$0.00018
10% off
32,768
None
StripedHyena Hessian 7B (base)
togethercomputer/stripedhyena-hessian-7b	
$0.00018
10% off
$0.00018
10% off
32,768
None
Mixtral 8x7B (base)
mistralai/mixtral-8x7b	
$0.00054
10% off
$0.00054
10% off
32,768
None
Nous: Hermes 2 Yi 34B
nousresearch/nous-hermes-yi-34b	
$0.00072
10% off
$0.00072
10% off
4,096
None
Nous: Hermes 2 Mixtral 8x7B SFT
nousresearch/nous-hermes-2-mixtral-8x7b-sft	
$0.00054
10% off
$0.00054
10% off
32,000
None
Nous: Hermes 2 Mistral 7B DPO
nousresearch/nous-hermes-2-mistral-7b-dpo	
$0.00018
10% off
$0.00018
10% off
8,192
None
Mistral OpenOrca 7B
open-orca/mistral-7b-openorca	
$0.0001425
5% off
$0.0001425
5% off
8,192
None
Hugging Face: Zephyr 7B
huggingfaceh4/zephyr-7b-beta	
$0.0001425
5% off
$0.0001425
5% off
4,096
None
OpenAI: GPT-3.5 Turbo
openai/gpt-3.5-turbo	
$0.0005
$0.0015
16,385
Moderated
OpenAI: GPT-3.5 Turbo 16k
openai/gpt-3.5-turbo-0125	
$0.0005
$0.0015
16,385
Moderated
OpenAI: GPT-3.5 Turbo 16k
openai/gpt-3.5-turbo-16k	
$0.003
$0.004
16,385
Moderated
OpenAI: GPT-4 Turbo
openai/gpt-4-turbo	
$0.01
$0.03
128,000
Moderated
OpenAI: GPT-4 Turbo Preview
openai/gpt-4-turbo-preview	
$0.01
$0.03
128,000
Moderated
OpenAI: GPT-4
openai/gpt-4	
$0.03
$0.06
8,191
Moderated
OpenAI: GPT-4 32k
openai/gpt-4-32k	
$0.06
$0.12
32,767
Moderated
OpenAI: GPT-4 Vision
openai/gpt-4-vision-preview	
$0.01
$0.03
128,000
Moderated
OpenAI: GPT-3.5 Turbo Instruct
openai/gpt-3.5-turbo-instruct	
$0.0015
$0.002
4,095
Moderated
Google: PaLM 2 Chat
google/palm-2-chat-bison	
$0.00025
$0.0005
25,804
None
Google: PaLM 2 Code Chat
google/palm-2-codechat-bison	
$0.00025
$0.0005
20,070
None
Google: PaLM 2 Chat 32k
google/palm-2-chat-bison-32k	
$0.00025
$0.0005
91,750
None
Google: PaLM 2 Code Chat 32k
google/palm-2-codechat-bison-32k	
$0.00025
$0.0005
91,750
None
Google: Gemini Pro 1.0
google/gemini-pro	
$0.000125
$0.000375
91,728
None
Google: Gemini Pro Vision 1.0
google/gemini-pro-vision	
$0.000125
$0.000375
45,875
None
Google: Gemini Pro 1.5 (preview)
google/gemini-pro-1.5	
$0.0025
$0.0075
2,800,000
None
Perplexity: PPLX 70B Online
perplexity/pplx-70b-online	
$0.001
$0.001
4,096
None
Perplexity: PPLX 7B Online
perplexity/pplx-7b-online	
$0.0002
$0.0002
4,096
None
Perplexity: PPLX 7B Chat
perplexity/pplx-7b-chat	
$0.0002
$0.0002
8,192
None
Perplexity: PPLX 70B Chat
perplexity/pplx-70b-chat	
$0.001
$0.001
4,096
None
Perplexity: Sonar 7B
perplexity/sonar-small-chat	
$0.0002
$0.0002
16,384
None
Perplexity: Sonar 8x7B
perplexity/sonar-medium-chat	
$0.0006
$0.0006
16,384
None
Perplexity: Sonar 7B Online
perplexity/sonar-small-online	
$0.0002
$0.0002
12,000
None
Perplexity: Sonar 8x7B Online
perplexity/sonar-medium-online	
$0.0006
$0.0006
12,000
None
Anthropic: Claude 3 Opus
anthropic/claude-3-opus	
$0.015
$0.075
200,000
Moderated
Anthropic: Claude 3 Sonnet
anthropic/claude-3-sonnet	
$0.003
$0.015
200,000
Moderated
Anthropic: Claude 3 Haiku
anthropic/claude-3-haiku	
$0.00025
$0.00125
200,000
Moderated
Anthropic: Claude 3 Opus (self-moderated)
anthropic/claude-3-opus:beta	
$0.015
$0.075
200,000
None
Anthropic: Claude 3 Sonnet (self-moderated)
anthropic/claude-3-sonnet:beta	
$0.003
$0.015
200,000
None
Anthropic: Claude 3 Haiku (self-moderated)
anthropic/claude-3-haiku:beta	
$0.00025
$0.00125
200,000
None
Meta: Llama v2 70B Chat
meta-llama/llama-2-70b-chat	
$0.0006
$0.0019
4,096
None
Nous: Capybara 34B
nousresearch/nous-capybara-34b	
$0.0009
$0.0009
32,768
None
Airoboros 70B
jondurbin/airoboros-l2-70b	
$0.0007
$0.0009
4,096
None
Bagel 34B v0.2
jondurbin/bagel-34b	
$0.00575
$0.00575
8,000
None
Chronos Hermes 13B v2
austism/chronos-hermes-13b	
$0.00018
$0.00018
4,096
None
Mistral 7B Instruct
mistralai/mistral-7b-instruct	
$0.0001
$0.00025
32,768
None
OpenChat 3.5
openchat/openchat-7b	
$0.00013
$0.00013
8,192
None
Toppy M 7B
undi95/toppy-m-7b	
$0.00015
$0.00015
4,096
None
lzlv 70B
lizpreciatior/lzlv-70b-fp16-hf	
$0.0007
$0.0008
4,096
None
Mixtral 8x7B Instruct
mistralai/mixtral-8x7b-instruct	
$0.00024
$0.00024
32,768
None
Dolphin 2.6 Mixtral 8x7B 🐬
cognitivecomputations/dolphin-mixtral-8x7b	
$0.0005
$0.0005
32,000
None
Noromaid Mixtral 8x7B Instruct
neversleep/noromaid-mixtral-8x7b-instruct	
$0.008
$0.008
8,000
None
Nous: Hermes 2 Mixtral 8x7B DPO
nousresearch/nous-hermes-2-mixtral-8x7b-dpo	
$0.0003
$0.0005
32,000
None
RWKV v5 World 3B
rwkv/rwkv-5-world-3b	
$0
$0
10,000
None
RWKV v5 3B AI Town
recursal/rwkv-5-3b-ai-town	
$0
$0
10,000
None
RWKV v5: Eagle 7B
recursal/eagle-7b	
$0
$0
10,000
None
Google: Gemma 7B
google/gemma-7b-it	
$0.0001
$0.0001
8,192
None
Databricks: DBRX 132B Instruct
databricks/dbrx-instruct	
$0.0006
$0.0006
32,768
None
Zephyr 141B-A35B
huggingfaceh4/zephyr-orpo-141b-a35b	
$0.00065
$0.00065
65,536
None
Meta: Llama 3 8B Instruct
meta-llama/llama-3-8b-instruct	
$0.0001
$0.0001
8,192
None
Meta: Llama 3 70B Instruct
meta-llama/llama-3-70b-instruct	
$0.0008
$0.0008
8,192
None
WizardLM-2 8x22B
microsoft/wizardlm-2-8x22b	
$0.00065
$0.00065
65,536
None
WizardLM-2 7B
microsoft/wizardlm-2-7b	
$0.0001
$0.0001
32,000
None
Mistral: Mixtral 8x22B (base)
mistralai/mixtral-8x22b	
$0.0009
$0.0009
65,536
None
Mistral: Mixtral 8x22B Instruct
mistralai/mixtral-8x22b-instruct	
$0.00065
$0.00065
65,536
None
Anthropic: Claude v2
anthropic/claude-2	
$0.008
$0.024
200,000
Moderated
Anthropic: Claude v2.1
anthropic/claude-2.1	
$0.008
$0.024
200,000
Moderated
Anthropic: Claude v2.0
anthropic/claude-2.0	
$0.008
$0.024
100,000
Moderated
Anthropic: Claude Instant v1
anthropic/claude-instant-1	
$0.0008
$0.0024
100,000
Moderated
Anthropic: Claude Instant v1.2
anthropic/claude-instant-1.2	
$0.0008
$0.0024
100,000
Moderated
Anthropic: Claude v2 (self-moderated)
anthropic/claude-2:beta	
$0.008
$0.024
200,000
None
Anthropic: Claude v2.1 (self-moderated)
anthropic/claude-2.1:beta	
$0.008
$0.024
200,000
None
Anthropic: Claude v2.0 (self-moderated)
anthropic/claude-2.0:beta	
$0.008
$0.024
100,000
None
Anthropic: Claude Instant v1 (self-moderated)
anthropic/claude-instant-1:beta	
$0.0008
$0.0024
100,000
None
Hugging Face: Zephyr 7B (free)
huggingfaceh4/zephyr-7b-beta:free	
$0
$0
4,096
None
Mixtral 8x7B Instruct (nitro)
mistralai/mixtral-8x7b-instruct:nitro	
$0.0005
$0.0005
32,768
None
Meta: Llama v2 70B Chat (nitro)
meta-llama/llama-2-70b-chat:nitro	
$0.0009
$0.0009
4,096
None
MythoMax 13B (nitro)
gryphe/mythomax-l2-13b:nitro	
$0.0002
$0.0002
4,096
None
Mistral 7B Instruct (nitro)
mistralai/mistral-7b-instruct:nitro	
$0.0002
$0.0002
32,768
None
Google: Gemma 7B (nitro)
google/gemma-7b-it:nitro	
$0.0002
$0.0002
8,192
None
Toppy M 7B (nitro)
undi95/toppy-m-7b:nitro	
$0.00015
$0.00015
4,096
None
WizardLM-2 8x22B (nitro)
microsoft/wizardlm-2-8x22b:nitro	
$0.001
$0.001
65,536
None
Meta: Llama 3 8B Instruct (nitro)
meta-llama/llama-3-8b-instruct:nitro	
$0.0002
$0.0002
8,192
None
Meta: Llama 3 70B Instruct (nitro)
meta-llama/llama-3-70b-instruct:nitro	
$0.0009
$0.0009
8,192
None
Mistral Tiny
mistralai/mistral-tiny	
$0.00025
$0.00025
32,000
None
Mistral Small
mistralai/mistral-small	
$0.002
$0.006
32,000
None
Mistral Medium
mistralai/mistral-medium	
$0.0027
$0.0081
32,000
None
Mistral Large
mistralai/mistral-large	
$0.008
$0.024
32,000
None
Cohere: Command
cohere/command	
$0.001
$0.002
4,096
None
Cohere: Command R
cohere/command-r	
$0.0005
$0.0015
128,000
None
Cohere: Command R+
cohere/command-r-plus	
$0.003
$0.015
128,000
None

Older versions
Media models
OpenAI: Shap-e
openai/shap-e
$0.01 / 32 steps
Note: Different models tokenize text in different ways. Some models break up text into chunks of multiple characters (GPT, Claude, Llama, etc) while others tokenize by character (PaLM). This means that the number of tokens may vary depending on the model.

Provider Routing
OpenRouter routes each request to the best available model provider for your preferences. You can customize them using the provider object in the request body. Here are the available options:

Custom Provider Selection
You can set the providers that OpenRouter will use for your request using the order field. The router will filter this list to only include providers that are available for the model you're using, and then try one at a time, failing if none are available. If you don't set this field, the router will use the default ordering shown on the model page.

typescript

Copy
fetch("https://openrouter.ai/api/v1/chat/completions", {
  method: "POST",
  headers: {
    "Authorization": `Bearer ${OPENROUTER_API_KEY}`,
    "HTTP-Referer": `${YOUR_SITE_URL}`, // Optional, for including your app on openrouter.ai rankings.
    "X-Title": `${YOUR_SITE_NAME}`, // Optional. Shows in rankings on openrouter.ai.
    "Content-Type": "application/json"
  },
  body: JSON.stringify({
    "model": "mistralai/mixtral-8x7b-instruct",
    "messages": [
      {"role": "user", "content": "Hello"},
    ],
    "provider": {
      "order": [
        "Azure",
        "Together"
      ]
    },
  })
});
Required Parameters (beta)
By default, providers that don't support a given LLM parameter will ignore them. But you can change this and only filter for providers that support the parameters in your request.

For example, to only use providers that support JSON formatting:

typescript

Copy
fetch("https://openrouter.ai/api/v1/chat/completions", {
  method: "POST",
  headers: {
    "Authorization": `Bearer ${OPENROUTER_API_KEY}`,
    "HTTP-Referer": `${YOUR_SITE_URL}`, // Optional, for including your app on openrouter.ai rankings.
    "X-Title": `${YOUR_SITE_NAME}`, // Optional. Shows in rankings on openrouter.ai.
    "Content-Type": "application/json"
  },
  body: JSON.stringify({
    "model": "mistralai/mixtral-8x7b-instruct",
    "messages": [
      {"role": "user", "content": "Hello"},
    ],
    "provider": {
      "require_parameters": true
    },
    "response_format": {
      "type": "json_object"
    },
  })
});
Data Privacy
Some model providers may log prompts, so we display them with a Data Policy tag on model pages. This is not a definitive source of third party data policies, but represents our best knowledge.

OpenRouter's data policy is managed on your Account page. You can disable logging there to also disable third party model providers that store logs for purposes like training. Alternatively, you can skip them on a per-request basis:

typescript

Copy
fetch("https://openrouter.ai/api/v1/chat/completions", {
  method: "POST",
  headers: {
    "Authorization": `Bearer ${OPENROUTER_API_KEY}`,
    "HTTP-Referer": `${YOUR_SITE_URL}`, // Optional, for including your app on openrouter.ai rankings.
    "X-Title": `${YOUR_SITE_NAME}`, // Optional. Shows in rankings on openrouter.ai.
    "Content-Type": "application/json"
  },
  body: JSON.stringify({
    "model": "mistralai/mixtral-8x7b-instruct",
    "messages": [
      {"role": "user", "content": "Hello"},
    ],
    "provider": {
      "data_collection": "deny"
    },
  })
});
Disabling a provider causes the router to skip over it and proceed to the next best one.

Disabling Fallbacks
To guarantee that your request is only served by the top (lowest-cost) provider, you can disable fallbacks:

typescript

Copy
fetch("https://openrouter.ai/api/v1/chat/completions", {
  method: "POST",
  headers: {
    "Authorization": `Bearer ${OPENROUTER_API_KEY}`,
    "HTTP-Referer": `${YOUR_SITE_URL}`, // Optional, for including your app on openrouter.ai rankings.
    "X-Title": `${YOUR_SITE_NAME}`, // Optional. Shows in rankings on openrouter.ai.
    "Content-Type": "application/json"
  },
  body: JSON.stringify({
    "model": "mistralai/mixtral-8x7b-instruct",
    "messages": [
      {"role": "user", "content": "Hello"},
    ],
    "provider": {
      "allow_fallbacks": false
    },
  })
});
For a complete list of options, see this JSON schema:

javascript

Copy
{
  "$ref": "#/definitions/ProviderPreferences",
  "definitions": {
    "ProviderPreferences": {
      "type": "object",
      "properties": {
        "allow_fallbacks": {
          "type": "boolean",
          "description": "Whether to allow backup providers to serve requests
- true: (default) when the primary provider is unavailable, use the next best provider.
- false: use only the primary provider, and return the upstream error if it's unavailable.
",
          "default": true
        },
        "require_parameters": {
          "type": "boolean",
          "description": "Whether to filter providers to only those that support the parameters you've provided. If this setting is omitted or set to false, then providers will receive only the parameters they support, and ignore the rest.",
          "default": false
        },
        "data_collection": {
          "type": "string",
          "enum": [
            "deny",
            "allow"
          ],
          "description": "Data collection setting. If no available model provider meets the requirement, your request will return an error.
- allow: (default) allow providers which store user data non-transiently and may train on it
- deny: use only providers which do not collect user data.
",
          "default": "allow"
        },
        "order": {
          "type": "array",
          "items": {
            "type": "string",
            "enum": [
              "OpenAI",
              "Anthropic",
              "HuggingFace",
              "Google",
              "Mancer",
              "Mancer 2",
              "Together",
              "DeepInfra",
              "Azure",
              "Modal",
              "AnyScale",
              "Replicate",
              "Perplexity",
              "Recursal",
              "Fireworks",
              "Mistral",
              "Groq",
              "Cohere",
              "Lepton",
              "OctoAI",
              "Novita",
              "Lynn"
            ]
          },
          "description": "An ordered list of provider names. The router will attempt to use the first provider in the subset of this list that supports your requested model, and fall back to the next if it is unavailable. If no providers are available, the request will fail with an error message."
        }
      },
      "additionalProperties": false
    }
  },
  "$schema": "http://json-schema.org/draft-07/schema#"
}
Model Routing
Multi-model routing is under development 👀

In the meantime, OpenRouter provides two options:

The Auto router, a special model ID that you can use to choose between selected high-quality models based on heuristics applied to your prompt.

The models array, which lets you automatically try other models if the primary model's providers are down, rate-limited, or refuse to reply due to content moderation required by all providers:

json

{
  "models": ["anthropic/claude-2.1", "gryphe/mythomax-l2-13b"],
  "route": "fallback",
  ... // Other params
}
If the model you selected returns an error, OpenRouter will try to use the fallback model instead. If the fallback model is down or returns an error, OpenRouter will return that error.

By default, any error can trigger the use of a fallback model, including context length validation errors, moderation flags for filtered models, rate-limiting, and downtime.

Requests are priced using the model that was used, which will be returned in the model attribute of the response body.

If no fallback model is specified but route: "fallback" is still included, OpenRouter will try the most appropriate open-source model available, with pricing less than the primary model (or very close to it).

OAuth PKCE
Users can connect to OpenRouter in one click using Proof Key for Code Exchange (PKCE). Here's an example, and here's a step-by-step:

Send your user to https://openrouter.ai/auth?callback_url=YOUR_SITE_URL

You can optionally include a code_challenge (random password up to 256 digits) for extra security.
For maximum security, we recommend also setting code_challenge_method to S256, and then setting code_challenge to the base64 encoding of the sha256 hash of code_verifier, which you will submit in Step 2. More info in Auth0's docs.
Once logged in, they'll be redirected back to your site with a code in the URL. Make an API call (can be frontend or backend) to exchange the code for a user-controlled API key. And that's it for PKCE!

Look for the code query parameter, e.g. ?code=....
typescript

fetch("https://openrouter.ai/api/v1/auth/keys", {
  method: 'POST',
  body: JSON.stringify({
    code: $CODE_FROM_QUERY_PARAM,
    code_verifier: $CODE_VERIFIER // Only needed if you sent a code_challenge in Step 1
  })
});
A fresh API key will be in the result under "key". Store it securely and make OpenAI-style requests (supports streaming as well):
typescript

Copy
fetch("https://openrouter.ai/api/v1/chat/completions", {
  method: "POST",
  headers: {
    "Authorization": `Bearer ${OPENROUTER_API_KEY}`,
    "HTTP-Referer": `${YOUR_SITE_URL}`, // Optional, for including your app on openrouter.ai rankings.
    "X-Title": `${YOUR_SITE_NAME}`, // Optional. Shows in rankings on openrouter.ai.
    "Content-Type": "application/json"
  },
  body: JSON.stringify({
    "model": "anthropic/claude-2",
    "messages": [
      {"role": "system", "content": "You are a helpful assistant."},
      {"role": "user", "content": "Hello!"},
    ],
  })
});
You can use JavaScript or any server-side framework, like Streamlit. The linked example shows multiple models and file Q&A.

API Keys
Users or developers can cover model costs with normal API keys. This allows you to use curl or the OpenAI SDK directly with OpenRouter. Just create an API key, set the api_base, and optionally set a referrer header to make your app discoverable to others on OpenRouter.

Note: API keys on OpenRouter are more powerful than keys used directly for model APIs. They allow users to set credit limits for apps, and they can be used in OAuth flows.

Example code:

python
typescript
shell

Copy
import openai

openai.api_base = "https://openrouter.ai/api/v1"
openai.api_key = $OPENROUTER_API_KEY

response = openai.ChatCompletion.create(
  model="openai/gpt-3.5-turbo",
  messages=[...],
  headers={
    "HTTP-Referer": $YOUR_SITE_URL, # Optional, for including your app on openrouter.ai rankings.
    "X-Title": $YOUR_APP_NAME, # Optional. Shows in rankings on openrouter.ai.
  },
)

reply = response.choices[0].message
To stream with Python, see this example from OpenAI.

Requests
OpenRouter's request and response schemas are very similar to the OpenAI Chat API, with a few small differences. At a high level, OpenRouter normalizes the schema across models and providers so you only need to learn one.

Request Body
Here's the request schema as a TypeScript type. This will be the body of your POST request to the /api/v1/chat/completions endpoint (see the quick start above for an example).

typescript

// Definitions of subtypes are below
type Request = {
  // Either "messages" or "prompt" is required
  messages?: Message[];
  prompt?: string;

  // If "model" is unspecified, uses the user's default
  model?: string; // See "Supported Models" section

  // Allows to force the model to produce specific output format.
  // Only supported by OpenAI models, Nitro models, and some others - check the
  // providers on the model page on openrouter.ai/models to see if it's supported,
  // and set `require_parameters` to true in your Provider Preferences. See
  // openrouter.ai/docs#provider-routing
  response_format?: { type: 'json_object' };

  stop?: string | string[];
  stream?: boolean; // Enable streaming

  // See LLM Parameters (openrouter.ai/docs#parameters)
  max_tokens?: number; // Range: [1, context_length)
  temperature?: number; // Range: [0, 2]
  top_p?: number; // Range: (0, 1]
  top_k?: number; // Range: [1, Infinity) Not available for OpenAI models
  frequency_penalty?: number; // Range: [-2, 2]
  presence_penalty?: number; // Range: [-2, 2]
  repetition_penalty?: number; // Range: (0, 2]
  seed?: number; // OpenAI only

  // Function-calling
  // Only natively suported by OpenAI models. For others, we submit
  // a YAML-formatted string with these tools at the end of the prompt.
  tools?: Tool[];
  tool_choice?: ToolChoice;

  // Additional optional parameters
  logit_bias?: { [key: number]: number };

  // OpenRouter-only parameters
  // See "Prompt Transforms" section: openrouter.ai/docs#transforms
  transforms?: string[];
  // See "Model Routing" section: openrouter.ai/docs#model-routing
  models?: string[];
  route?: 'fallback';
  // See "Provider Routing" section: openrouter.ai/docs#provider-routing
  provider?: ProviderPreferences;
};

// Subtypes:

type TextContent = {
  type: 'text';
  text: string;
};

type ImageContentPart = {
  type: 'image_url';
  image_url: {
    url: string; // URL or base64 encoded image data
    detail?: string; // Optional, defaults to 'auto'
  };
};

type ContentPart = TextContent | ImageContentPart;

type Message = {
  role: 'user' | 'assistant' | 'system' | 'tool';
  // ContentParts are only for the 'user' role:
  content: string | ContentPart[];
  // If "name" is included, it will be prepended like this
  // for non-OpenAI models: `{name}: {content}`
  name?: string;
};

type FunctionDescription = {
  description?: string;
  name: string;
  parameters: object; // JSON Schema object
};

type Tool = {
  type: 'function';
  function: FunctionDescription;
};

type ToolChoice =
  | 'none'
  | 'auto'
  | {
      type: 'function';
      function: {
        name: string;
      };
    };
Request Headers
OpenRouter allows you to specify an optional HTTP-Referer header to identify your app and make it discoverable to users on openrouter.ai. You can also include an optional X-Title header to set or modify the title of your app. Example:

javascript

Copy
fetch("https://openrouter.ai/api/v1/chat/completions", {
  method: "POST",
  headers: {
    "Authorization": `Bearer ${OPENROUTER_API_KEY}`,
    "HTTP-Referer": `${YOUR_SITE_URL}`, // Optional, for including your app on openrouter.ai rankings.
    "X-Title": `${YOUR_SITE_NAME}`, // Optional. Shows in rankings on openrouter.ai.
    "Content-Type": "application/json"
  },
  body: JSON.stringify({
    "model": "mistralai/mixtral-8x7b-instruct",
    "messages": [
      {"role": "user", "content": "Who are you?"},
    ],
  })
});
Model routing: If the model parameter is omitted, the user or payer's default is used. Otherwise, remember to select a value for model from the supported models or API, and include the organization prefix. OpenRouter will select the least expensive and best GPUs available to serve the request, and fall back to other providers or GPUs if it receives a 5xx response code or if you are rate-limited.

Streaming: Server-Sent Events (SSE) are supported as well, to enable streaming for all models. Simply send stream: true in your request body. The SSE stream will occasionally contain a "comment" payload, which you should ignore (noted below).

Non-standard parameters: If the chosen model doesn't support a request parameter (such as logit_bias in non-OpenAI models, or top_k for OpenAI), then the parameter is ignored. The rest are forwarded to the underlying model API.

Assistant Prefill: OpenRouter supports asking models to complete a partial response. This can be useful for guiding models to respond in a certain way.

To use this features, simply include a message with role: "assistant" at the end of your messages array. Example:

javascript

Copy
fetch("https://openrouter.ai/api/v1/chat/completions", {
  method: "POST",
  headers: {
    "Authorization": `Bearer ${OPENROUTER_API_KEY}`,
    "HTTP-Referer": `${YOUR_SITE_URL}`, // Optional, for including your app on openrouter.ai rankings.
    "X-Title": `${YOUR_SITE_NAME}`, // Optional. Shows in rankings on openrouter.ai.
    "Content-Type": "application/json"
  },
  body: JSON.stringify({
    "model": "mistralai/mixtral-8x7b-instruct",
    "messages": [
      {"role": "user", "content": "Who are you?"},
      {"role": "assistant", "content": "I'm not sure, but my best guess is"},
    ],
  })
});
Stream Cancellation
For some providers, streaming requests can be canceled by aborting the connection or simply disconnecting.

When aborting the connection to a provider that supports stream cancellation, the model will stop processing the request, and billing will stop as soon as the upstream provider detects the disconnection.

If you're using the Fetch API, you can use the AbortController to cancel the stream. Here's an example:

typescript

const controller = new AbortController();

fetch('https://openrouter.ai/api/v1/chat/completions', {
  method: 'POST',
  headers: ...,
  body: ...,
  signal: controller.signal
})

...

// Later, to cancel the stream:
controller.abort();
NOTE: Aborting/disconnecting from a non-stream request or a stream request to a provider that does not support stream cancellation will not halt the model's processing in the background. You will still be billed for the rest of the completion.

Responses
Responses are largely consistent with the OpenAI Chat API. This means that choices is always an array, even if the model only returns one completion. Each choice will contain a delta property if a stream was requested and a message property otherwise. This makes it easier to use the same code for all models.

At a high level, OpenRouter normalizes the schema across models and providers so you only need to learn one.

Response Body
Note that finish_reason will vary depending on the model provider. The model property tells you which model was used inside the underlying API.

Here's the response schema as a TypeScript type:

typescript

// Definitions of subtypes are below

type Response = {
  id: string;
  // Depending on whether you set "stream" to "true" and
  // whether you passed in "messages" or a "prompt", you
  // will get a different output shape
  choices: (NonStreamingChoice | StreamingChoice | NonChatChoice | Error)[];
  created: number; // Unix timestamp
  model: string;
  object: 'chat.completion' | 'chat.completion.chunk';
  // For non-streaming responses only. For streaming responses,
  // see "Querying Cost and Stats" below.
  usage?: {
    completion_tokens: number; // Equivalent to "native_tokens_completion" in the /generation API
    prompt_tokens: number; // Equivalent to "native_tokens_prompt"
    total_tokens: number; // Sum of the above two fields
    total_cost: number; // Number of credits used by this generation
  };
};

// Subtypes:

type NonChatChoice = {
  finish_reason: string | null;
  text: string;
};

type NonStreamingChoice = {
  finish_reason: string | null; // Depends on the model. Ex: 'stop' | 'length' | 'content_filter' | 'tool_calls' | 'function_call'
  message: {
    content: string | null;
    role: string;
    tool_calls?: ToolCall[];
    // Deprecated, replaced by tool_calls
    function_call?: FunctionCall;
  };
};

type StreamingChoice = {
  finish_reason: string | null;
  delta: {
    content: string | null;
    role?: string;
    tool_calls?: ToolCall[];
    // Deprecated, replaced by tool_calls
    function_call?: FunctionCall;
  };
};

type Error = {
  code: number; // See "Error Handling" section
  message: string;
};

type FunctionCall = {
  name: string;
  arguments: string; // JSON format arguments
};

type ToolCall = {
  id: string;
  type: 'function';
  function: FunctionCall;
};
Here's an example:

json

{
  "id": "gen-xxxxxxxxxxxxxx",
  "choices": [
    {
      "finish_reason": "stop", // Different models provide different reasons here
      "message": {
        // will be "delta" if streaming
        "role": "assistant",
        "content": "Hello there!"
      }
    }
  ],
  "model": "openai/gpt-3.5-turbo" // Could also be "anthropic/claude-2.1", etc, depending on the "model" that ends up being used
}
Querying Cost and Stats
You can use the returned id to query for the generation stats (including token counts and cost) after the request is complete. This is how you can get the cost and tokens for all models and requests, streaming and non-streaming.

javascript

const generation = await fetch(
  "https://openrouter.ai/api/v1/generation?id=$GENERATION_ID",
  { headers }
)

await generation.json()
// OUTPUT:
{
  data: {
    "id": "gen-nNPYi0ZB6GOK5TNCUMHJGgXo",
    "model": "openai/gpt-4-32k",
    "streamed": false,
    "generation_time": 2,
    "created_at": "2023-09-02T20:29:18.574972+00:00",
    "tokens_prompt": 24,
    "tokens_completion": 29,
    "native_tokens_prompt": 24,
    "native_tokens_completion": 29,
    "num_media_prompt": null,
    "num_media_completion": null,
    "origin": "https://localhost:47323/",
    "total_cost": 0.00492
  }
};
Note that token counts and total_cost are also available in the usage field of the response body for non-streaming completions.

SSE Streaming Comments
For SSE streams, we occasionally need to send an SSE comment to indicate that OpenRouter is processing your request. This helps prevent connections from timing out. The comment will look like this:


Copy
: OPENROUTER PROCESSING
Comment payload can be safely ignored per the SSE specs. However, you can leverage it to improve UX as needed, e.g. by showing a dynamic loading indicator.

Some SSE client implementations might not parse the payload according to spec, which leads to an uncaught error when you JSON.stringify the non-JSON payloads. We recommend the following clients:

eventsource-parser
OpenAI SDK
Vercel AI SDK
LLM Parameters

temperature
Optional, float, 0.0 to 2.0

Default: 1.0

Explainer Video: Watch

This setting influences the variety in the model's responses. Lower values lead to more predictable and typical responses, while higher values encourage more diverse and less common responses. At 0, the model always gives the same response for a given input.


top_p
Optional, float, 0.0 to 1.0

Default: 1.0

Explainer Video: Watch

This setting limits the model's choices to a percentage of likely tokens: only the top tokens whose probabilities add up to P. A lower value makes the model's responses more predictable, while the default setting allows for a full range of token choices. Think of it like a dynamic Top-K.


top_k
Optional, integer, 0 or above

Default: 0

Explainer Video: Watch

This limits the model's choice of tokens at each step, making it choose from a smaller set. A value of 1 means the model will always pick the most likely next token, leading to predictable results. By default this setting is disabled, making the model to consider all choices.


frequency_penalty
Optional, float, -2.0 to 2.0

Default: 0.0

Explainer Video: Watch

This setting aims to control the repetition of tokens based on how often they appear in the input. It tries to use less frequently those tokens that appear more in the input, proportional to how frequently they occur. Token penalty scales with the number of occurrences. Negative values will encourage token reuse.


presence_penalty
Optional, float, -2.0 to 2.0

Default: 0.0

Explainer Video: Watch

Adjusts how often the model repeats specific tokens already used in the input. Higher values make such repetition less likely, while negative values do the opposite. Token penalty does not scale with the number of occurrences. Negative values will encourage token reuse.


repetition_penalty
Optional, float, 0.0 to 2.0

Default: 1.0

Explainer Video: Watch

Helps to reduce the repetition of tokens from the input. A higher value makes the model less likely to repeat tokens, but too high a value can make the output less coherent (often with run-on sentences that lack small words). Token penalty scales based on original token's probability.


min_p
Optional, float, 0.0 to 1.0

Default: 0.0

Represents the minimum probability for a token to be considered, relative to the probability of the most likely token. (The value changes depending on the confidence level of the most probable token.) If your Min-P is set to 0.1, that means it will only allow for tokens that are at least 1/10th as probable as the best possible option.


top_a
Optional, float, 0.0 to 1.0

Default: 0.0

Consider only the top tokens with "sufficiently high" probabilities based on the probability of the most likely token. Think of it like a dynamic Top-P. A lower Top-A value focuses the choices based on the highest probability token but with a narrower scope. A higher Top-A value does not necessarily affect the creativity of the output, but rather refines the filtering process based on the maximum probability.


seed
Optional, integer
If specified, the inferencing will sample deterministically, such that repeated requests with the same seed and parameters should return the same result. Determinism is not guaranteed for some models.


max_tokens
Optional, integer, 1 or above
This sets the upper limit for the number of tokens the model can generate in response. It won't produce more than this limit. The maximum value is the context length minus the prompt length.


logit_bias
Optional, map
Accepts a JSON object that maps tokens (specified by their token ID in the tokenizer) to an associated bias value from -100 to 100. Mathematically, the bias is added to the logits generated by the model prior to sampling. The exact effect will vary per model, but values between -1 and 1 should decrease or increase likelihood of selection; values like -100 or 100 should result in a ban or exclusive selection of the relevant token.


logprobs
Optional, boolean
Whether to return log probabilities of the output tokens or not. If true, returns the log probabilities of each output token returned.


top_logprobs
Optional, integer
An integer between 0 and 20 specifying the number of most likely tokens to return at each token position, each with an associated log probability. logprobs must be set to true if this parameter is used.


response_format
Optional, map
Forces the model to produce specific output format. Setting to { "type": "json_object" } enables JSON mode, which guarantees the message the model generates is valid JSON. Note: when using JSON mode, you should also instruct the model to produce JSON yourself via a system or user message.


stop
Optional, array
Stop generation immediately if the model encounter any token specified in the stop array.

Parameters API
OpenRouter Parameters API
 1.0.0 
OAS 3.1
This API lets you query the top LLM sampling parameter configurations used by users on OpenRouter.


Authorize
default


GET
/api/v1/parameters/{modelId}


Prompt Transforms
OpenRouter has a simple rule for choosing between sending a prompt and sending a list of ChatML messages:

Choose messages if you want to have OpenRouter apply a recommended instruct template to your prompt, depending on which model serves your request. Available instruct modes include:
alpaca: docs
llama2: docs
airoboros: docs
Choose prompt if you want to send a custom prompt to the model. This is useful if you want to use a custom instruct template or maintain full control over the prompt submitted to the model.
To help with prompts that exceed the maximum context size of a model, OpenRouter supports a custom parameter called transforms:

typescript

{
  transforms: ["middle-out"], // Compress prompts > context size. This is the default for all models.
  messages: [...], // "prompt" works as well
  model // Works with any model
}
The transforms param is an array of strings that tell OpenRouter to apply a series of transformations to the prompt before sending it to the model. Transformations are applied in-order. Available transforms are:

middle-out: compress prompts and message chains to the context size. This helps users extend conversations in part because LLMs pay significantly less attention to the middle of sequences anyway. Works by compressing or removing messages in the middle of the prompt.
Note: All OpenRouter models default to using middle-out, unless you exclude this transform by e.g. setting transforms: [] in the request body.

Error Handling
For errors, OpenRouter returns a JSON response with the following shape:

typescript

type ErrorResponse = {
  error: {
    code: number;
    message: string;
    metadata?: Record<string, unknown>;
  };
};
The HTTP Response will have the same status code as error.code, forming a request error if:

Your original request is invalid
Your API key/account is out of credits
Otherwise, the returned HTTP response status will be 200 and any error occured while the LLM is producing the output will be emitted in the response body or as an SSE data event.

Example code for printing errors in JavaScript:

javascript

const request = await fetch('https://openrouter.ai/...');
console.log(request.status); // Will be an error code unless the model started processing your request
const response = await request.json();
console.error(response.error?.status); // Will be an error code
console.error(response.error?.message);
Error Codes
400: Bad Request (invalid or missing params, CORS)
401: Invalid credentials (OAuth session expired, disabled/invalid API key)
402: Your account or API key has insufficient credits. Add more credits and retry the request.
403: Your chosen model requires moderation and your input was flagged
408: Your request timed out
429: You are being rate limited
502: Your chosen model is down or we received an invalid response from it
503: There is no available model provider that meets your routing requirements
Moderation Errors
If your input was flagged, the error metadata will contain information about the issue. The shape of the metadata is as follows:

typescript

type ModerationErrorMetadata = {
  reasons: string[]; // Why your input was flagged
  flagged_input: string; // The text segment that was flagged, limited to 100 characters. If the flagged input is longer than 100 characters, it will be truncated in the middle and replaced with ...
};
Limits
Rate Limits and Credits Remaining
To check the rate limit or credits left on an API key, make a GET request to https://openrouter.ai/api/v1/auth/key.

javascript

fetch('https://openrouter.ai/api/v1/auth/key', {
  method: 'GET',
  headers: {
    Authorization: 'Bearer $OPENROUTER_API_KEY'
  }
});
If you submit a valid API key, you should get a response of the form:

typescript

type Key = {
  data: {
    label: string;
    usage: number; // Number of credits used
    limit: number | null; // Credit limit for the key, or null if unlimited
    is_free_tier: boolean; // Whether the user has paid for credits before
    rate_limit: {
      requests: number; // Number of requests allowed...
      interval: string; // in this interval, e.g. "10s"
    };
  };
};
There are two global rate limits which apply to all requests, regardless of account status or model availability:

Surge limit: By default, all users are subject to a maximum rate limit of 200 requests per second to defend against denial-of-service attacks. Contact us in Discord or using our support@ email address if you need a higher limit.

Free limit: If you are using a free model variant (with an ID ending in :free), then you will be limited to 10 requests per minute and 100 requests per day.

For all other requests, rate limits are a function of the number of credits remaining on the key or account. For the credits available on your API key, you can make 1 request per credit per second up to the surge limit.

For example:

0 credits → 1 req/s (minimum)
5 credits → 5 req/s
10 credits → 10 req/s
1000 credits → 200 req/s (maximum)
If your account has a negative credit balance, you may see 402 errors, including for free models. Adding credits to put your balance above zero allows you to use those models again.

Token Limits
Some users may have too few credits on their account to make expensive requests. OpenRouter provides a way to know that before making a request to any model.

To get the maximum tokens that a user can generate and the maximum tokens allowed in their prompt, add authentication headers in your request to https://openrouter.ai/api/v1/models:

javascript

fetch('https://openrouter.ai/api/v1/models', {
  method: 'GET',
  headers: {
    Authorization: 'Bearer $OPENROUTER_API_KEY'
  }
});
Each model will include a per_request_limits property:

typescript

type Model = {
  id: string;
  pricing: {
    prompt: number;
    completion: number;
  };
  context_length: number;
  per_request_limits: {
    prompt_tokens: number;
    completion_tokens: number;
  };
};
Other Frameworks
You can find a few examples of using OpenRouter with other frameworks in this Github repository. Here are some examples:

Using npm i openai: github.

Tip: You can also use Grit to automatically migrate your code. Simply run npx @getgrit/launcher openrouter.
Using Streamlit: github

Using LangChain for Python: github

Using LangChain.js: github

javascript

Copy
const chat = new ChatOpenAI({
  modelName: "anthropic/claude-instant-v1",
  temperature: 0.8,
  streaming: true,
  openAIApiKey: $OPENROUTER_API_KEY,
}, {
  basePath: $OPENROUTER_BASE_URL + "/api/v1",
  baseOptions: {
    headers: {
      "HTTP-Referer": "https://yourapp.com/", // Optional, for including your app on openrouter.ai rankings.
      "X-Title": "Langchain.js Testing", // Optional. Shows in rankings on openrouter.ai.
    },
  },
});
Using the Vercel AI SDK:
javascript

Copy
const config = new Configuration({
  basePath: $OPENROUTER_BASE_URL + "/api/v1",
  apiKey: $OPENROUTER_API_KEY,
  baseOptions: {
    headers: {
      "HTTP-Referer": "https://yourapp.com/", // Optional, for including your app on openrouter.ai rankings.
      "X-Title": "Vercel Testing", // Optional. Shows in rankings on openrouter.ai.
    }
  }
})

const openrouter = new OpenAIApi(config)
3D Objects (beta)
OpenRouter supports text-to-3D Object generation, currently in beta. See supported media models and try a demo. To generate 3D Objects, send a POST request to https://openrouter.ai/api/v1/objects/generations

shell

curl https://openrouter.ai/api/v1/objects/generations \\
  -H "Content-Type: application/json" \\
  -H "Authorization: Bearer $OPENROUTER_API_KEY" \\
  -H "HTTP-Referer: $YOUR_SITE_URL" \\
  -H "X-Title: $YOUR_SITE_NAME" \\
  -d '{
    "prompt": "a chair shaped like an avacado",
    "num_inference_steps": 32,
    "num_outputs": 1,
    "extension": "ply",
    "model": "openai/shap-e"
  }'
You should recieve a response of type MediaResponse:

typescript

//Each generation will contain either a base64 string or a hosted url, or both.
interface MediaOutput {
  uri?: string; //base64 string
  url?: string; //hosted url
};

interface MediaResponse {
  generations: MediaOutput[];
};
