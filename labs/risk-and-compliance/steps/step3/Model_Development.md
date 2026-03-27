# Model Developer's Guide to perform Model Developement on watsonx

## Overview

This repository contains the Model Developer's guide for AI Governance, focusing on automating HR policy question/answering processes using IBM watsonx **AutoRAG** capabilities.

## 1. Use Case

**Business Goal:** Automate question/answering process from HR policies using IBM watsonx **AutoRAG**, enabling faster, bias-free hiring while maintaining compliance in OpenPages.

### 🧠 Agentic RAG Capabilities for HR Policy Q&A:

1. Ingest and index HR policy documents (PDFs, DOCX, web pages, internal knowledge bases)
2. Allow users to ask natural language questions about HR policies (e.g., leave, benefits, conduct, compliance)
3. Retrieve relevant policies using semantic search
4. Generate clear, accurate answers grounded in official HR documentation
5. Highlight source references to support transparency and traceability
6. Support multilingual queries and inclusive language understanding

> **Note:** The Agentic RAG model for this use case is **already created and deployed** in the pre-production environment.

---

## 2. Persona

**Model Developer:** Responsible for accessing the deployed Agentic RAG model, running evaluations, and integrating outputs into OpenPages.

---

## 3. Step-by-Step OpenPages Flow

### **Step 1 – Access the Deployed Agentic RAG Model**

The Agentic RAG model is already developed and deployed. To access it:

1. Log in to the **[IBM Cloud](https://cloud.ibm.com/login)** platform.

<img width="800" alt="IBM Cloud Login" src="https://github.com/user-attachments/assets/0c1713aa-efaa-4856-b945-8b37e75be937" />


2. Open **hamburger menu → Resource List → watsonx.governance**
   
<img width="800" alt="Watsonx Governance Navigation" src="https://github.com/user-attachments/assets/70fae95e-0657-496c-b9e0-fb1fc9082d7d" />


3. Click the **Launch in watsonx.governance** button — this navigates to:
   [https://dataplatform.cloud.ibm.com/wx/home?context=wx](https://dataplatform.cloud.ibm.com/wx/home?context=wx)
   
<img width="800" alt="Launch watsonx.governance" src="https://github.com/user-attachments/assets/cadd8c90-2bff-442f-ad9f-99d73c660938" />



4. On the **watsonx Studio** homepage:
   
* Create a new project as explained in the steps linked here: [Steps for creating project](https://github.com/MEA-Watsonx-bootcamp-IBM/ai-governance-client-bootcamp/blob/main/labs/risk-and-compliance/instructor/create-project.md)
  
* After creating the project, go to the **Assets** tab and click on **New Asset**:
  
<img width="800" alt="New Asset Creation" src="https://github.com/user-attachments/assets/f623e6b2-61ce-4e15-8d81-52913ccdae1b" />

* Select **Working with data or models in Python or R notebooks** from the **All** option on the sidebar:
  
<img width="800" alt="Notebook Selection" src="https://github.com/user-attachments/assets/76b39a73-edd7-46d7-8b2f-cb816d33cf1d" />


* Go to the **local file** tab and click **browse** to upload the notebook linked here as a local file: [Notebook](https://github.com/MEA-Watsonx-bootcamp-IBM/ai-governance-client-bootcamp/blob/main/labs/risk-and-compliance/steps/step3/notebook/agentic-rag.ipynb)
  
<img width="800" alt="File Upload" src="https://github.com/user-attachments/assets/9a738df9-5c3c-47cf-b697-6aa0fd3db7ee" />



* Select the [Notebook](https://github.com/MEA-Watsonx-bootcamp-IBM/ai-governance-client-bootcamp/blob/main/labs/risk-and-compliance/steps/step3/notebook/agentic-rag.ipynb), download it locally, and upload it to the watsonx.ai runtime.
  
<img width="800" alt="Notebook Upload" src="https://github.com/user-attachments/assets/882f43cc-5006-4a77-a4e8-f95dec1cf910" />


* After uploading, provide a name to the notebook and click the **Create** button:
  
<img width="800" alt="Notebook Creation" src="https://github.com/user-attachments/assets/9b4b89e6-fb0f-4953-a70f-50184cacac9a" />


* The notebook will now be ready to run and **create a Detached Prompt Template for Agentic RAG** in the OpenScale dashboard UI

-> In this notebook:

- Use **watsonx_api_key** created initially [Create API key](https://github.com/MEA-Watsonx-bootcamp-IBM/ai-governance-client-bootcamp/blob/main/labs/risk-and-compliance/instructor/api_key_setup.md)
- Access **project_id** by navigating: hamburger menu → projects → view all projects → your project-> Manage tab -> copy project id.


<img width="800" alt="Notebook Ready" src="https://github.com/user-attachments/assets/14f551af-a4ee-46f8-9d6c-630b189d66a6" />

   
<img width="800" alt="Notebook Ready" src="https://github.com/user-attachments/assets/748f2258-3b2a-44e9-b85e-1ea0e8998173" />


---

> **Note:** The Model Developer can use this Notebook for evaluation and integration.

---

### **Step 2 – Run Notebook in watsonx.governance**

Run the above notebook and then visualize the results in **IBM watsonx Openscale** Dashboard:


#### Using the UI:


Navigate to the **Detached Prompt Template** asset within the project on **[Openscale](https://aiopenscale.cloud.ibm.com/aiopenscale/insights?nocache=true&bss_account=4b9fae855573451bb6e3bb27d9153c4a)** Dashboard:


<img width="800" alt="Detached Prompt Template UI" src="https://github.com/user-attachments/assets/9b3b5dff-79f0-4426-8773-e9b3a5acf0db" />



### **Step 3 – AI Factsheet View of Detached Prompt Template **


1. Go to dataplatform.cloud.ibm.com watsonx studio

<img width="800" alt="Detached Prompt Template UI" src="https://github.com/user-attachments/assets/df4f17d8-f16e-4949-8130-7d33a9443580" />



2. Navigate: hamburger menu → projects → view all projects → HR Process Automation (select this project)

   
<img width="800" alt="Detached Prompt Template UI" src="https://github.com/user-attachments/assets/d79437d4-efb5-4a42-a83f-05b8571dda29" />




3. Inside this project, you will find **Detached prompt template** named **Agentic RAG** - select that

   
<img width="800" alt="Detached Prompt Template UI" src="https://github.com/user-attachments/assets/c7d99704-06d7-4087-9974-4e410524a5a1" />




4. After selecting, you will be onboarded to **AI Factsheet**


<img width="800" alt="Detached Prompt Template UI" src="https://github.com/user-attachments/assets/395af2af-49e6-4d17-b0a3-75a14c6fd7b8" />




5. Now click on **Track in AI use case**  to associate asset to **AI Use case** click on **Go to AI Use cases** as project is not associated to **AI Use case** :


<img width="800" alt="Detached Prompt Template UI" src="https://github.com/user-attachments/assets/fda39ce4-8a73-4eb7-9be4-d5de3b81945e" />




6. Select **AI Use case** created by **Use case owner** initially :


<img width="800" alt="Detached Prompt Template UI" src="https://github.com/user-attachments/assets/06315d79-772c-41a2-98be-d843231cef4c" />




7. Go to **Associated workspaces** section and Select **Validation** phase and click on **Associate Workspace**:


<img width="800" alt="Detached Prompt Template UI" src="https://github.com/user-attachments/assets/1e984eee-534a-40c3-a2d2-ebaab2a3cc1b" />




9. Here, Select **Project** created initially and Deployment space created  or if you have not created Click on **+New Space** and follow [Deployment Creation Steps](https://github.com/MEA-Watsonx-bootcamp-IBM/ai-governance-client-bootcamp/blob/main/labs/risk-and-compliance/instructor/deploy-project.md) these steps for creating deployment space for **Testing** Deployment stage. Click on Save:


<img width="800" alt="Detached Prompt Template UI" src="https://github.com/user-attachments/assets/187b363b-0ccc-44f6-a7db-0ea65728f36d" />




10. Now **AI Use case** is associated to **project** and **deployment space**.In **Associated Workspaces** Section Click on Arrow beside **your project** under **Validation** phase:


    
<img width="800" alt="Detached Prompt Template UI" src="https://github.com/user-attachments/assets/feb1f6ed-864d-496a-8b7d-242d2c65090f" />




11. In project go to **Assets** tab select **Agentic RAG testing** asset and click on three dot then select **Go to AI factsheet**



<img width="800" alt="Detached Prompt Template UI" src="https://github.com/user-attachments/assets/cd0643a9-ddd7-4a1f-b8a5-b846a9a17116" />



12. Now **AI Use case** is getting tracked in **Validation** phase so Click on **Track in AI Use case**:


<img width="800" alt="Detached Prompt Template UI" src="https://github.com/user-attachments/assets/7e6739d1-2973-4d6c-af2d-774e93175f62" />




13. Select Approach set as **Default Approach** or click on **+New Approach** for defining one path for solving the goal of the use case. Click on **Next**:



<img width="800" alt="Detached Prompt Template UI" src="https://github.com/user-attachments/assets/b6bb9e83-ae46-4661-967f-f8c9bd260b07" />



<img width="800" alt="Detached Prompt Template UI" src="https://github.com/user-attachments/assets/1f9cb12a-8c92-46f2-9cd7-1d38f2b587a1" />



14. Associate the **asset** with an existing model record or create a new model record in OpenPages. This will sync the tracked model facts between Model inventory and OpenPages.Click on **Next**.


<img width="800" alt="Detached Prompt Template UI" src="https://github.com/user-attachments/assets/3d3c2141-95a8-47f4-8c43-64a2c177e2be" />




15. Choose the starting point for this approach(Experimental,Stable,Custom) any one of them for **version** tracking. Click on **Next**:


<img width="800" alt="Detached Prompt Template UI" src="https://github.com/user-attachments/assets/68000588-deeb-4bbb-9731-4dcb7ee1de5a" />



16. Review to make sure that your detached prompt template is stable before you track it in an **AI use case**. Click on **Track Asset**:


<img width="800" alt="Detached Prompt Template UI" src="https://github.com/user-attachments/assets/dc8266fd-bc48-4bc4-8d2d-13bdedc46a17" />




Finally **Agentic RAG** getting tracked in **AI Use case**. Click on **Agentic RAG Testing** under asset record to view it in **Governance Console**


<img width="800" alt="Detached Prompt Template UI" src="https://github.com/user-attachments/assets/2b7b9657-e31b-4f74-ad18-42fb85001448" />



<img width="800" alt="Detached Prompt Template UI" src="https://github.com/user-attachments/assets/e856e5d8-82fc-44e4-8b51-777a44a222ec" />



17. Now go back to the [Model Developer Tasks Guide](../step3/model-developer-tasks.md) to finish the developement declaration and start the validation process.

> [!Note]
> Model Developer has developed **Agentic RAG Detached prompt template** and Also onboarded it to **AI Use case**

---

## Prerequisites

- IBM Cloud account with access to watsonx.governance
- Access to the pre-deployed Agentic RAG model
- Permissions to create and manage projects in Watsonx Studio

## Resources

- [IBM Cloud Platform](https://cloud.ibm.com/login)
- [Project Creation Steps](../../instructor/create-project.md)
- [Create API key](../../instructor/api_key_setup.md)
- [Agentic RAG Notebook - Dallas](./notebook/agentic-rag.ipynb)
