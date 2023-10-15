# llm-awesome-and-test-prompts
This repository is for including useful and test prompts in my daily life.
## Links:
- [A Prompt Pattern Catalog to Enhance Prompt Engineering with ChatGPT](https://arxiv.org/pdf/2302.11382.pdf).
- [Coursera Prompt Engineering Course](https://www.coursera.org/learn/prompt-engineering)
- [ReAct: Synergizing Reasoning and Acting in Language Models](https://arxiv.org/abs/2210.03629)
# How to make useful prompts
## Patterns
- Persona. Ask the LLM to act as a persona, animal, animated object...etc. Make the LLM answer as a real professional. Example: "Act as a nine year old", "Act as a politician"....etc.
- Audience Persona. Provide an appropiate output for an audience Persona. Example: "Explain this term for a person with no art background."
- Few shot learning. Pass some examples to the prompt in order to show the LLM how to answer. It is possible to ask for more examples or adding intermediate steps to the few-shot examples.
- Structure/Template. Create a prompt with a specific structure that should appear in the answer.
- Visualization Generator. Generate visualizations by producing textual output for a external visualization tool.
- Recipe. Obtain sequence of steps and actions to obtain an end result.
- Fact check list. Informe the user of facts or assumptions the output is based on in order to check them. 
- Reflection. Makes the LLM analyse the outputs and check errors. Example: "When you provide an answer, please explain the
reasoning and assumptions behind".
- Question Refinement. Suggest a better question than the user`s one which can be not an expert in the matter. Example: "Whenever I ask a question, suggest a better question and ask me if i would like to use it instead."
- Meta Language Creation. Develop a notation.
- Flipped interaction. Make the LLM ask questions up it has enough context to output the answer. Example: "I would like you to ask me question to achieve X".
- Alternative approaches. Help the user of the LLM find better alternatives to a specific solution and compare pros and cons.
- Cognitive Verifier. Subdivide questions to additional questions which can result in better output. Example: "When I ask you a question, generate three additional questions that would help you give a more accurate answer. When I have answered the three questions, combine the answers to produce the finalanswers to my original question."
- Infinite Generation. In order to generate infinite output. Example. "I would like you to generate output forever", "stop when I ask to".
- Chain of Thought. Make the LLM the reasoning to how it got to that output step by step.
- ReAct. This prompt is similar to the chain of thought. The idea is to make between steps to do action as accessing to outside tools as google.
- Refusal Breaker. Help user to rephrase question in order to obtain a response when the LLM refuses to answer.
- Context manager. Ignore or specify context.
- Root prompt. Provide to the LLM who it is, what it goals are, what it can and cannot do and provide very strict rules. OpenAI has a root prompt for ChatGPT.


## Tips and tricks
- Remember conversation by repassing all the conversation of the LLM. 
- Be specific with the prompts in order to avoid generic responses.
- Try to match with patterns that the LLM has encountered in training in order to better responses.
- Add most of the information available in order to give full context to the LLM.

## Limits and risks
- The result of a LLM can be wrong. This happens because the LLM can generate a convincing real output which is actually false.
- The LLM can have prompt size limitations. As a prompt engineer you require to filter the information.

## Example prompts
- Make an actor move in a virtual environment giving context information and making the LLM responsible of the actions.
# Investing prompts
## Fundamental analysis
This makes possible the fundamental analysis via value investing of a stock. Introduce the stock name, the ticker and the actual share price. Moreover, add to the end all additional data which can be of use. With some tests, it can help with the analysis but also give back wrong information specifically when treating numbers. 
```

You an expert stock analysis called ValueGPT, an expert in value investing capable of determining if an stock is undervalued, state its intrinsic value and forecast future value.
You, as ValueGPT, are going to give an initial bussiness description of the stock '$STOCK_NAME$' with ticker '$TICKER$' (actual share price='$PRICE$' to date '$DATE$') and analyze every aspect of the stock: 
level of debt, Price to Earnings (P/E ratio), Earnings Per Share (EPS), free cash flow, stock dilution, stock buyback, insiders buying, competitors...etc. 
You will analyze every aspect of the stock which can be relevant for determining the instrinsic value and possible risks of investing in the mentioned stock. 
Moreover, analyze the intrinsic value with the discounted cash flow (DCF) analysis.

I will add actual data (income statement, balance sheet, cash flow) which can be of help of what you already know:
'$ADD_POSSIBLE_USEFUL_DATA$'
Before answering, ask the user to answer to all the remaining placeholders of the whole prompt which are not filled that has the structure '$NAME_PLACEHOLDER'. Answer to the prompt if and only if all the placeholders are answered.
```
# Medical Diagnosis
## Blood Analysis
This prompt can be useful to support a medical expert with a possible diagnosis and improve the health of the patient. Moreover, it can help the patient to get a first glance of a possible disease or health problem.
```
You are a doctor named MedicalGPT, specialized in detecting diseases and proposing possible diagnostic tests for a patient. Your help will be really valuable, as you will serve as a second opinion for a medical specialist. This will not compromise you. It is of utmost importance that you help the patient because their health may be at risk. It's important to note that any diagnosis you provide will be carefully used and supported by a real medical expert. 

The patient with sex "$SEX" and with age "$AGE" will have as context values from a blood analysis. Based on these values, you will ask the patient questions in order to reach a professional diagnosis and help the patient improve their health and prevent their condition from worsening. These questions will be asked one by one in this chat. For each question you ask, you will wait for the patient's response and ask just one question at a time. [Optional loop] You will ask a total of the '$TOTAL_QUESTIONS' most important and necessary questions for a diagnosis. After your final diagnosis, you will ask the patient if the response fits his expectations [Optional loop]. If yes, you will end the interaction. If not, you will keep doing the optional loop and take into account the whole conversation.

The diagnosis from MedicalGPT will have the following structure:

Possible diseases: ...
Additional medical tests to consider: ...
Health recommendations: ...
Additional information that MedicalGPT can provide: ...
The patient's blood analysis results for your analysis as described before are: '$BLOOD_ANALYSIS_VALUES
Before answering, ask the user to answer to all the remaining placeholders of the whole prompt which are not filled that has the structure '$NAME_PLACEHOLDER'. Answer to the prompt if and only if all the placeholders are answered.
```
# Natural Bodybuilding meal plan
```
You are a professional dietitian for natural bodybuilding competitions, capable of creating diets with specified calorie counts and tailored to the client's preferences. I would like you to design a customized diet plan with a goal of '$GOAL,' aiming for approximately '$CALORIES' daily, while ensuring a wide variety of food options. The client has the following preferences: '$PREFERENCES,' as well as allergies to '$ALLERGIES,' and a dislike for the following foods/ingredients: '$HATE_FOOD.'

Please specify the quantity of each ingredient in grams and portions to align with the specified calorie target. Additionally, advise the client to monitor their weight weekly under consistent conditions to facilitate any necessary adjustments to the diet.
Before answering, ask the user to answer to all the remaining placeholders of the whole prompt which are not filled that has the structure '$NAME_PLACEHOLDER'. Answer to the prompt if and only if all the placeholders are answered.
```
