<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "9b03446058b4eed46928ae5e46325ea0",
  "translation_date": "2025-10-02T13:49:23+00:00",
  "source_file": "00-course-setup/README.md",
  "language_code": "bn"
}
-->
# কোর্স সেটআপ

## পরিচিতি

এই পাঠে আমরা দেখব কীভাবে এই কোর্সের কোড নমুনাগুলি চালানো যায়।

## অন্যান্য শিক্ষার্থীদের সাথে যোগ দিন এবং সাহায্য পান

আপনার রিপোজিটরি ক্লোন করার আগে, [AI Agents For Beginners Discord চ্যানেলে](https://aka.ms/ai-agents/discord) যোগ দিন। এখানে আপনি সেটআপে সাহায্য, কোর্স সম্পর্কিত প্রশ্ন, বা অন্যান্য শিক্ষার্থীদের সাথে সংযোগ স্থাপন করতে পারবেন।

## এই রিপোজিটরি ক্লোন বা ফর্ক করুন

শুরু করার জন্য, অনুগ্রহ করে GitHub রিপোজিটরি ক্লোন বা ফর্ক করুন। এটি আপনার নিজস্ব কোর্স উপকরণের সংস্করণ তৈরি করবে যাতে আপনি কোড চালাতে, পরীক্ষা করতে এবং পরিবর্তন করতে পারেন!

এটি করতে <a href="https://github.com/microsoft/ai-agents-for-beginners/fork" target="_blank">রিপোজিটরি ফর্ক করার</a> লিঙ্কে ক্লিক করুন।

এখন আপনার কাছে এই কোর্সের ফর্ক করা সংস্করণ থাকবে নিম্নলিখিত লিঙ্কে:

![Forked Repo](../../../translated_images/forked-repo.33f27ca1901baa6a5e13ec3eb1f0ddd3a44d936d91cc8cfb19bfdb9688bd2c3d.bn.png)

## কোড চালানো

এই কোর্সে Jupyter Notebooks-এর একটি সিরিজ রয়েছে যা আপনাকে AI Agents তৈরি করার হাতে-কলম অভিজ্ঞতা দেবে।

কোড নমুনাগুলি নিম্নলিখিত ব্যবহার করে:

**GitHub অ্যাকাউন্ট প্রয়োজন - বিনামূল্যে**:

1) Semantic Kernel Agent Framework + GitHub Models Marketplace। লেবেল করা হয়েছে (semantic-kernel.ipynb)
2) AutoGen Framework + GitHub Models Marketplace। লেবেল করা হয়েছে (autogen.ipynb)

**Azure সাবস্ক্রিপশন প্রয়োজন**:
3) Azure AI Foundry + Azure AI Agent Service। লেবেল করা হয়েছে (azureaiagent.ipynb)

আমরা আপনাকে তিনটি উদাহরণই চেষ্টা করার পরামর্শ দিই যাতে আপনি দেখতে পারেন কোনটি আপনার জন্য সবচেয়ে ভালো কাজ করে।

আপনি যেটি বেছে নেবেন, সেটি নির্ধারণ করবে নিচের সেটআপ ধাপগুলি:

## প্রয়োজনীয়তা

- Python 3.12+
  - **NOTE**: যদি আপনার কাছে Python3.12 ইনস্টল না থাকে, নিশ্চিত করুন যে আপনি এটি ইনস্টল করেছেন। তারপর requirements.txt ফাইল থেকে সঠিক সংস্করণগুলি ইনস্টল করতে python3.12 ব্যবহার করে আপনার venv তৈরি করুন।
  
    >উদাহরণ

    Python venv ডিরেক্টরি তৈরি করুন:

    ``` bash
    python3 -m venv venv
    ```

    তারপর venv পরিবেশ সক্রিয় করুন:

    macOS এবং Linux

    ```bash
    source venv/bin/activate
    ```
  
    Windows

    ```bash
    venv\Scripts\activate
    ```

- একটি GitHub অ্যাকাউন্ট - GitHub Models Marketplace-এ অ্যাক্সেসের জন্য
- Azure সাবস্ক্রিপশন - Azure AI Foundry-এ অ্যাক্সেসের জন্য
- Azure AI Foundry অ্যাকাউন্ট - Azure AI Agent Service-এ অ্যাক্সেসের জন্য

আমরা এই রিপোজিটরির মূল অংশে একটি `requirements.txt` ফাইল অন্তর্ভুক্ত করেছি যা কোড নমুনাগুলি চালানোর জন্য প্রয়োজনীয় সমস্ত Python প্যাকেজ ধারণ করে।

আপনি এটি ইনস্টল করতে পারেন আপনার টার্মিনালে নিম্নলিখিত কমান্ড চালিয়ে:

```bash
pip install -r requirements.txt
```
আমরা কোনো দ্বন্দ্ব এবং সমস্যা এড়াতে একটি Python ভার্চুয়াল পরিবেশ তৈরি করার সুপারিশ করি।

## VSCode সেটআপ
নিশ্চিত করুন যে আপনি VSCode-এ সঠিক Python সংস্করণ ব্যবহার করছেন।

![image](https://github.com/user-attachments/assets/a85e776c-2edb-4331-ae5b-6bfdfb98ee0e)

## GitHub Models ব্যবহার করে নমুনার সেটআপ 

### ধাপ ১: আপনার GitHub Personal Access Token (PAT) সংগ্রহ করুন

এই কোর্স GitHub Models Marketplace ব্যবহার করে, যা আপনাকে বিনামূল্যে Large Language Models (LLMs) অ্যাক্সেস প্রদান করে যা আপনি AI Agents তৈরি করতে ব্যবহার করবেন।

GitHub Models ব্যবহার করতে, আপনাকে একটি [GitHub Personal Access Token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens) তৈরি করতে হবে।

এটি আপনার GitHub অ্যাকাউন্টের <a href="https://github.com/settings/personal-access-tokens" target="_blank">Personal Access Tokens settings</a> এ গিয়ে করা যেতে পারে।

অনুগ্রহ করে [Principle of Least Privilege](https://docs.github.com/en/get-started/learning-to-code/storing-your-secrets-safely) অনুসরণ করুন যখন আপনি আপনার টোকেন তৈরি করবেন। এর অর্থ হলো টোকেনকে শুধুমাত্র সেই অনুমতিগুলি দিন যা এই কোর্সের কোড নমুনাগুলি চালানোর জন্য প্রয়োজন।

1. **Developer settings**-এ গিয়ে স্ক্রিনের বাম পাশে `Fine-grained tokens` অপশনটি নির্বাচন করুন।
   ![](../../../translated_images/profile_developer_settings.410a859fe749c755c859d414294c5908e307222b2c61819c3203bbeed4470e25.bn.png)

    তারপর `Generate new token` নির্বাচন করুন।

    ![Generate Token](../../../translated_images/fga_new_token.1c1a234afe202ab37483944a291ee80c1868e1e78082fd6bd4180fea5d5a15b4.bn.png)

2. আপনার টোকেনের জন্য একটি বর্ণনামূলক নাম লিখুন যা এর উদ্দেশ্য প্রতিফলিত করে, যাতে এটি পরে সহজে চিহ্নিত করা যায়।

    🔐 টোকেনের মেয়াদকাল সুপারিশ

    সুপারিশকৃত মেয়াদকাল: ৩০ দিন  
    আরও নিরাপদ অবস্থানের জন্য, আপনি একটি ছোট সময়কাল বেছে নিতে পারেন—যেমন ৭ দিন 🛡️  
    এটি একটি ব্যক্তিগত লক্ষ্য নির্ধারণ করার এবং কোর্স সম্পন্ন করার একটি দুর্দান্ত উপায় 🚀।

    ![Token Name and Expiration](../../../translated_images/token-name-expiry-date.a095fb0de63868640a4c82d6b1bbc92b482930a663917a5983a3c7cd1ef86b77.bn.png)

3. টোকেনের স্কোপ আপনার এই রিপোজিটরির ফর্কে সীমাবদ্ধ করুন।

    ![Limit scope to fork repository](../../../translated_images/token_repository_limit.924ade5e11d9d8bb6cd21293987e4579dea860e2ba66d607fb46e49524d53644.bn.png)

4. টোকেনের অনুমতিগুলি সীমিত করুন: **Permissions** এর অধীনে **Account** ট্যাবটি ক্লিক করুন এবং "+ Add permissions" বোতামটি ক্লিক করুন। একটি ড্রপডাউন উপস্থিত হবে। অনুগ্রহ করে **Models** অনুসন্ধান করুন এবং এটি চেক করুন।
    ![Add Models Permission](../../../translated_images/add_models_permissions.c0c44ed8b40fc143dc87792da9097d715b7de938354e8f771d65416ecc7816b8.bn.png)

5. টোকেন তৈরি করার আগে প্রয়োজনীয় অনুমতিগুলি যাচাই করুন। ![Verify Permissions](../../../translated_images/verify_permissions.06bd9e43987a8b219f171bbcf519e45ababae35b844f5e9757e10afcb619b936.bn.png)

6. টোকেন তৈরি করার আগে নিশ্চিত করুন যে আপনি এটি একটি নিরাপদ স্থানে সংরক্ষণ করতে প্রস্তুত, যেমন একটি পাসওয়ার্ড ম্যানেজার ভল্ট, কারণ এটি তৈরি করার পরে এটি আবার দেখানো হবে না। ![Store Token Securely](../../../translated_images/store_token_securely.08ee2274c6ad6caf3482f1cd1bad7ca3fdca1ce737bc485bfa6499c84297c789.bn.png)

আপনার সদ্য তৈরি করা টোকেনটি কপি করুন। এখন এটি এই কোর্সে অন্তর্ভুক্ত `.env` ফাইলে যোগ করুন।

### ধাপ ২: আপনার `.env` ফাইল তৈরি করুন

আপনার টার্মিনালে নিম্নলিখিত কমান্ড চালিয়ে `.env` ফাইল তৈরি করুন।

```bash
cp .env.example .env
```

এটি উদাহরণ ফাইলটি কপি করবে এবং আপনার ডিরেক্টরিতে একটি `.env` তৈরি করবে যেখানে আপনি পরিবেশ ভেরিয়েবলগুলির জন্য মানগুলি পূরণ করবেন।

আপনার টোকেনটি কপি করে, আপনার প্রিয় টেক্সট এডিটরে `.env` ফাইলটি খুলুন এবং `GITHUB_TOKEN` ফিল্ডে আপনার টোকেনটি পেস্ট করুন।  
![GitHub Token Field](../../../translated_images/github_token_field.20491ed3224b5f4ab24d10ced7a68c4aba2948fe8999cfc8675edaa16f5e5681.bn.png)

এখন আপনি এই কোর্সের কোড নমুনাগুলি চালাতে সক্ষম হবেন।

## Azure AI Foundry এবং Azure AI Agent Service ব্যবহার করে নমুনার সেটআপ

### ধাপ ১: আপনার Azure প্রকল্পের এন্ডপয়েন্ট সংগ্রহ করুন

Azure AI Foundry-এ একটি হাব এবং প্রকল্প তৈরি করার ধাপগুলি অনুসরণ করুন এখানে: [Hub resources overview](https://learn.microsoft.com/en-us/azure/ai-foundry/concepts/ai-resources)

আপনার প্রকল্প তৈরি করার পরে, আপনাকে আপনার প্রকল্পের সংযোগ স্ট্রিং সংগ্রহ করতে হবে।

এটি Azure AI Foundry পোর্টালের **Overview** পৃষ্ঠায় গিয়ে করা যেতে পারে।

![Project Connection String](../../../translated_images/project-endpoint.8cf04c9975bbfbf18f6447a599550edb052e52264fb7124d04a12e6175e330a5.bn.png)

### ধাপ ২: আপনার `.env` ফাইল তৈরি করুন

আপনার টার্মিনালে নিম্নলিখিত কমান্ড চালিয়ে `.env` ফাইল তৈরি করুন।

```bash
cp .env.example .env
```

এটি উদাহরণ ফাইলটি কপি করবে এবং আপনার ডিরেক্টরিতে একটি `.env` তৈরি করবে যেখানে আপনি পরিবেশ ভেরিয়েবলগুলির জন্য মানগুলি পূরণ করবেন।

আপনার টোকেনটি কপি করে, আপনার প্রিয় টেক্সট এডিটরে `.env` ফাইলটি খুলুন এবং `PROJECT_ENDPOINT` ফিল্ডে আপনার টোকেনটি পেস্ট করুন।

### ধাপ ৩: Azure-এ সাইন ইন করুন

নিরাপত্তার সেরা অনুশীলন হিসাবে, আমরা [keyless authentication](https://learn.microsoft.com/azure/developer/ai/keyless-connections?tabs=csharp%2Cazure-cli?WT.mc_id=academic-105485-koreyst) ব্যবহার করব Microsoft Entra ID দিয়ে Azure OpenAI-তে প্রমাণীকরণের জন্য।

পরবর্তী ধাপে, একটি টার্মিনাল খুলুন এবং `az login --use-device-code` চালিয়ে আপনার Azure অ্যাকাউন্টে সাইন ইন করুন।

আপনি লগ ইন করার পরে, টার্মিনালে আপনার সাবস্ক্রিপশন নির্বাচন করুন।

## অতিরিক্ত পরিবেশ ভেরিয়েবল - Azure Search এবং Azure OpenAI 

Agentic RAG পাঠ - পাঠ ৫ - এর জন্য কিছু নমুনা রয়েছে যা Azure Search এবং Azure OpenAI ব্যবহার করে।

যদি আপনি এই নমুনাগুলি চালাতে চান, তাহলে আপনাকে `.env` ফাইলে নিম্নলিখিত পরিবেশ ভেরিয়েবলগুলি যোগ করতে হবে:

### Overview Page (Project)

- `AZURE_SUBSCRIPTION_ID` - **Overview** পৃষ্ঠার **Project details** চেক করুন।

- `AZURE_AI_PROJECT_NAME` - আপনার প্রকল্পের **Overview** পৃষ্ঠার শীর্ষে দেখুন।

- `AZURE_OPENAI_SERVICE` - **Overview** পৃষ্ঠার **Included capabilities** ট্যাবে **Azure OpenAI Service** এর জন্য এটি খুঁজুন।

### Management Center

- `AZURE_OPENAI_RESOURCE_GROUP` - **Management Center** এর **Overview** পৃষ্ঠার **Project properties** এ যান।

- `GLOBAL_LLM_SERVICE` - **Connected resources** এর অধীনে **Azure AI Services** সংযোগের নাম খুঁজুন। যদি তালিকাভুক্ত না থাকে, তাহলে **Azure portal**-এ আপনার রিসোর্স গ্রুপের অধীনে AI Services রিসোর্সের নাম চেক করুন।

### Models + Endpoints Page

- `AZURE_OPENAI_EMBEDDING_DEPLOYMENT_NAME` - আপনার embedding মডেল (যেমন, `text-embedding-ada-002`) নির্বাচন করুন এবং মডেল বিবরণ থেকে **Deployment name** নোট করুন।

- `AZURE_OPENAI_CHAT_DEPLOYMENT_NAME` - আপনার chat মডেল (যেমন, `gpt-4o-mini`) নির্বাচন করুন এবং মডেল বিবরণ থেকে **Deployment name** নোট করুন।

### Azure Portal

- `AZURE_OPENAI_ENDPOINT` - **Azure AI services** খুঁজুন, এটি ক্লিক করুন, তারপর **Resource Management**, **Keys and Endpoint**-এ যান, "Azure OpenAI endpoints"-এ স্ক্রোল করুন এবং "Language APIs" এর জন্য কপি করুন।

- `AZURE_OPENAI_API_KEY` - একই স্ক্রিন থেকে KEY 1 বা KEY 2 কপি করুন।

- `AZURE_SEARCH_SERVICE_ENDPOINT` - আপনার **Azure AI Search** রিসোর্স খুঁজুন, এটি ক্লিক করুন এবং **Overview** দেখুন।

- `AZURE_SEARCH_API_KEY` - তারপর **Settings** এবং **Keys**-এ যান এবং প্রাথমিক বা মাধ্যমিক অ্যাডমিন কী কপি করুন।

### External Webpage

- `AZURE_OPENAI_API_VERSION` - [API version lifecycle](https://learn.microsoft.com/en-us/azure/ai-services/openai/api-version-deprecation#latest-ga-api-release) পৃষ্ঠার **Latest GA API release** এর অধীনে যান।

### Keyless authentication সেটআপ করুন

আপনার শংসাপত্রগুলি হার্ডকোড করার পরিবর্তে, আমরা Azure OpenAI-এর সাথে একটি keyless সংযোগ ব্যবহার করব। এটি করতে, আমরা `DefaultAzureCredential` আমদানি করব এবং পরে `DefaultAzureCredential` ফাংশন কল করব শংসাপত্র পেতে।

```python
from azure.identity import DefaultAzureCredential, InteractiveBrowserCredential
```

## কোথাও আটকে গেছেন?

যদি আপনার এই সেটআপ চালাতে কোনো সমস্যা হয়, আমাদের <a href="https://discord.gg/kzRShWzttr" target="_blank">Azure AI Community Discord</a>-এ যোগ দিন অথবা <a href="https://github.com/microsoft/ai-agents-for-beginners/issues?WT.mc_id=academic-105485-koreyst" target="_blank">একটি সমস্যা তৈরি করুন</a>।

## পরবর্তী পাঠ

আপনি এখন এই কোর্সের কোড চালানোর জন্য প্রস্তুত। AI Agents-এর জগৎ সম্পর্কে আরও শিখতে শুভকামনা! 

[AI Agents এবং Agent Use Cases-এর পরিচিতি](../01-intro-to-ai-agents/README.md)

---

**অস্বীকৃতি**:  
এই নথিটি AI অনুবাদ পরিষেবা [Co-op Translator](https://github.com/Azure/co-op-translator) ব্যবহার করে অনুবাদ করা হয়েছে। আমরা যথাসাধ্য সঠিকতার জন্য চেষ্টা করি, তবে অনুগ্রহ করে মনে রাখবেন যে স্বয়ংক্রিয় অনুবাদে ত্রুটি বা অসঙ্গতি থাকতে পারে। মূল ভাষায় থাকা নথিটিকে প্রামাণিক উৎস হিসেবে বিবেচনা করা উচিত। গুরুত্বপূর্ণ তথ্যের জন্য, পেশাদার মানব অনুবাদ সুপারিশ করা হয়। এই অনুবাদ ব্যবহারের ফলে কোনো ভুল বোঝাবুঝি বা ভুল ব্যাখ্যা হলে আমরা দায়বদ্ধ থাকব না।