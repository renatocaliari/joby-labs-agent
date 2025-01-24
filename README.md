<table>
  <tr>
    <td colspan="2" style="text-align:center"><strong>👋 Hey! Cali from Brazil here! 🇧🇷</strong></td>
  </tr>
  <tr>
    <th style="text-align:center">Support this project</th>
    <th style="text-align:center">Connect with me</th>
  </tr>
  <tr>
    <td style="text-align:center; vertical-align:middle;">
      <a href="https://buymeacoffee.com/calirenato82">
        <img src="https://github.com/user-attachments/assets/b28741c6-5bc5-4bd1-a53a-9364a0acdf3d" alt="Buy me a coffee" width="26">
        <br>
        Buy me a coffee ☕
      </a>
    </td>
    <td style="text-align:center; vertical-align:middle;">
      <a href="https://www.linkedin.com/in/calirenato82">
        <img src="https://upload.wikimedia.org/wikipedia/commons/8/81/LinkedIn_icon.svg" alt="LinkedIn" width="38">
        <br>
        LinkedIn
      </a>
    </td>
  </tr>
</table>

# JTBD Mapper AI Agent 🤖 Free & Open-Source
_*Remember to periodically check for a new version_

<mark style="background: yellow; padding: 10px;">Important: Even though we use Visual Studio Code, a popular IDE among developers, you won't need to write a single line of code. All interactions will be through a chat interface with the Cline extension.</mark>

The "JTBD Mapper AI Agent" is designed to provide a comprehensive JTBD mapping, covering the key aspects, but it's not meant to be the definitive end of the analysis. Think of it as a research partner that helps you quickly map out the landscape.

It's crucial to remember that initial research findings, whether generated by AI or humans, should be critically evaluated and continually refined through ongoing investigation as new knowledge emerge.

You can leverage tools like Google 1.5 Pro with Deep Research or Perplexity for focused investigations, enabling you to gather potentially more up-to-date and contextualized information by 
exploring a wider range of sources and perspectives. You can also use NotebookLM to organize this research, input relevant references from the previous investigation and data from research studies, and collaborate with others to analyze and interpret the findings.

These are just a few examples of tools and how they can be integrated to support the work. A combination of AI-powered tools and human expertise.

This agent uses seriously powerful large language models – think Gemini 2.0, Qwen 2.5, and Llama 3.3 – that have been trained on tons of data. They can identify complex patterns and relationships in that data, which can be really helpful, even in specialized B2B contexts. They're great at finding patterns and making predictions, but they can also reflect biases present in the data they were trained on.

It's crucial to critically evaluate the results, just like you would with any research. This means checking for accuracy, considering potential biases, and identifying any limitations.
You can also refine the results by conducting further research with your target audience to validate and enrich the findings.

It's configured to work within [Cline](https://github.com/cline/cline), a free and open-source extension for VS Code — an IDE commonly used for systems development.
You can use free LLMs such as Gemini 2.0, Llama 3.3, and Qwen 2.5.

With this combination, you can have an autonomous agent that performs mapping autonomously. 
It only asks questions to confirm options you want to proceed with to the next stages.

# Installation

1. Open your terminal. Search for "terminal" or "command prompt" on your computer and open the appropriate application.

- Check if Git is installed: In your terminal, type `git --version` and press Enter. If any result appears showing the git version, then you have git installed. Otherwise, you do not have it

**If Git is installed:**

- Clone the repository. Type it in the terminal:

```git clone https://github.com/renatocaliari/JTBD-Mapper-AI-Agent.git```

- Now, type the following command:

```cd JTBD-Mapper-AI-Agent```

**If Git is not installed (or if the git --version command doesn't work):**

- Navigate to the desired directory: Use the `cd` command to navigate to the directory where you want to copy. For example, `cd ~/Downloads/JTBD-Mapper-AI-Agent` and press Enter.
- Run the following command: paste the following command into your terminal and press Enter:
```
curl https://raw.githubusercontent.com/renatocaliari/JTBD-Mapper-AI-Agent/main/script_setup.sh | bash
```
4. [Download VS Code and install](https://code.visualstudio.com/download).
5. Open VS Code.
6. [Install the extension Cline](https://marketplace.visualstudio.com/items?itemName=saoudrizwan.claude-dev).
7. Open Cline's settings, clicking on the gear icon. The icon is in the extension window, at the top on the left side.
![image](https://github.com/user-attachments/assets/1c259022-daf1-4c9e-9eb7-65f0e189fa77)


8. [Generate an API key in Google AI Studio](https://aistudio.google.com/app/apikey) to be able to use the LLM Google's Gemini for free.
     - Go to [Google AI Studio](https://aistudio.google.com/app/apikey).
     - Click on Create API Key.
     - Select the project "Generative Language Client" or any other with a free-of-charge plan.
     - Click on Create API key in existing project.
     - Click on Copy.
9. Go back to Cline's settings and select "Google Gemini" as the API Provider.
10. Paste the API key into the "Gemini API key" field. Then, select the "gemini-2.0-flash-thinking-exp-1219" model or a newer one, or any other you wish to try.
11. Click the File menu and then Open Folder. Find the folder you ran the script or cloned the repository and click to open the folder "JTBD-Mapper-AI-Agent".
12. Open the file custom_instructions.md and copy the content.
13. Paste the content copied in step 5 into Cline's Custom Instructions configuration.
14. Click DONE after finishing the settings.
15. In the Cline chat, check "Auto-approve: ..."
16. Then, intype a message like ```generate a job map for "xyz"``` and press Enter.
17. Your maps will be generated within the `result_docs` subdirectory created by the agent in the main directory with this format: `{currentdate_and_time}_{job to be done}_docs`.

# LLM Alternatives

## Free
You can use other providers to try different LLMs, like:

### mistral
To try Codestral 25.01 - from Mistral - free of charge, create an API key at `https://console.mistral.ai/api-keys/`. 

**It's important to know: **
Codestral 25.01 is specialized in tasks related to code generation and assistance, with a focus on improving developer productivity. However, it can function reasonably well for you to experiment with this agent.

Then, in Cline's settings, configure the provider to 'Mistral'. 

And paste your new api key in the Mistral Api Key.


### glhf.chat: Qwen and Llama
To try Llama 3.3 or Qwen 2.5 free of charge, create an API key at `https://glhf.chat/users/settings/api`. 

Then, in Cline's settings, configure the provider to 'OpenAI Compatible' and the Base URL to `https://glhf.chat/api/openai/v1`. 

Paste `hf:meta-llama/Llama-3.3-70B-Instruct` as the model to use Llama 3.3, or 'hf:Qwen/Qwen2.5-72B-Instruct' for Qwen 2.5.

### hyperbolic: DeepSeek V3, Qwen and Llama

To try DeepSeek V3, Llama 3.3 or Qwen 2.5 free of charge, create an API key at `https://app.hyperbolic.xyz/`. 

Then, in Cline's settings, configure the provider to 'OpenAI Compatible' and the Base URL to `https://api.hyperbolic.xyz/v1`. 

Paste `deepseek-ai/DeepSeek-V3` as the model to use DeepSeek V3.

## Cheap, but not free

### DeepSeek-V3 API

To try DeepSeek V3 API directly, create an API key at `https://platform.deepseek.com/api_keys`. 

Then, in Cline's settings, configure the provider to 'DeepSeek'.

Select `deepseek-chat` as the model to use DeepSeek V3.

# Troubleshooting

You might occasionally encounter an "API Request Failed" error with the message "Too many requests". 
This is a common occurrence with free usage plans, often due to rate limiting or resource exhaustion. To resolve this, simply wait a short period and then click "Retry." 

Google's Gemini 2.0 is a powerful LLM that is currently offered for free, making the occasional need to retry a reasonable trade-off.

![image](https://github.com/user-attachments/assets/2048aa50-ecef-4868-a6c5-8d11f91073d0)

Error content:
```
[GoogleGenerativeAI Error]: Error fetching from https://generativelanguage.googleapis.com/v1beta/models/gemini-2.0-flash-thinking-exp-1219:streamGenerateContent?alt=sse: [429 Too Many Requests] Resource has been exhausted (e.g. check quota)."
```

# Jobs To Be Done & Prompts 
- 🇺🇸 For more information on Jobs To Be Done, check out the [free e-book "Estratégia e Inovação baseadas em Jobs To Be Done" (Jobs To Be Done: Strategy and Innovation)](https://calirenato82.substack.com/p/e-book-jobs-to-be-done-em-portugues) (in Brazilian Portuguese, but you can translate it with Google Translate).
- 🇧🇷 Para mais informações sobre Jobs To Be Done, consulte o [e-book gratuito Estratégia e Inovação baseadas em Jobs To Be Done](https://calirenato82.substack.com/p/e-book-jobs-to-be-done-em-portugues).

# Example
The image below was created after mapping the "listen music" Job To Be Done. 

On the left side is the area where the AI interacts with us through the Cline interface, a VS Code extension. 

You can see the result of this mapping in the GitHub directory [`example/jtbd/listen to music`](https://github.com/renatocaliari/JTBD-Mapper-AI-Agent/tree/main/example/jtbd/listen%20to%20music).

![image](https://github.com/user-attachments/assets/41b0decc-3948-4a14-9611-adcb9c6716e4)
