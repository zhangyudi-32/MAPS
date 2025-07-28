# MAPS
> This software was developed as part of the study:  
> **_Leveraging LLM-based multi-agent simulations to boost participatory design education: An experimental exploration in residential area design_**
---

## 🖥️ Environment Setup

### Hardware Requirements
- A computer with at least a **dual-core 2.00 GHz CPU**
- **4GB RAM** or more

### Software Requirements
- **Windows 10** or above
- Active **internet connection**

---

## ⚙️ Installation Guide

### 1. Software Installation
Download the program package from the internet and unzip it. No installation is required—simply run the executable.

### 2. Software Configuration
This software requires access to a large language model (LLM) API provided by a cloud service provider.

Please:
- Apply for or purchase access to a provider (e.g., *SiliconFlow*)
- Fill in the following credentials in the `api_key.json` file:
  - `api_url`
  - `model_name`
  - `api_key`

### 3. Token Usage and Cost
Token usage depends on the **number of agents** and **rounds of dialogue**. Monitor your usage and cost based on your needs.

---

## 🧑‍🤝‍🧑 Population Profile Generation

1. Open `Population Profile Random Generator.xlsx`
2. Input demographic statistics of neighborhoods within the urban renewal area
3. The spreadsheet will generate a synthetic resident population profile

Copy the generated profiles into `agent_profile.xlsx` and add descriptions for additional roles like **government**, **developers**, etc. The system will automatically generate prompt templates for each role using this data.

---

## 🚀 System Features and Usage

Launch the software by running `MAPS.exe`. It will load the data from `agent_profile.xlsx` and initialize the intelligent agents. Below are the main features:

### 1. Introduce Project Background & Trigger Discussion

- Click **@All**
- Input background info about the urban renewal project
- All agents will receive this information
- Click **Free Discussion**, specify the number of speakers
- Agents will generate responses based on their profiles
- Discussion logs are automatically saved in the `/log` folder

### 2. Design Options & Analyze Needs

- Click **Multiple Choice**
- Enter a question (e.g., *"Which public service is most needed nearby?"*)
  - Refer to `[example] question_prompt.md` for templates
- The system will display the percentage of votes for options A, B, C, etc.
- Results are automatically saved in the `/output` folder

### 3. Scenario Discussion (Stakeholder Perspective Analysis)

- Click **Scenario Discussion**
- Input a scenario question (e.g., a planning dilemma or trade-off)
  - Refer to `[example] scenario_prompt.md`
- Agents will conduct structured discussions around key metrics and opinions

⏳ *Note: This process involves heavy API usage and may take over 15 minutes. Please be patient if the UI appears unresponsive.*

### 4. Upload Planning Schemes & Collect Feedback

- Use the **bottom-right section** of the interface to upload planning diagrams (e.g., images or PDFs)
- Ask for feedback from agents and review their responses
- Use the feedback to iteratively revise your proposal
- Repeat the process until reasonable consensus is reached

### 5. Save and Reload Dialogue History

- When closing the software, conversation logs are saved to the `/log` folder
- To reload a previous session, click **Load History**
- Select the corresponding `.txt` file to resume where you left off

---

## 📁 Folder Structure

```plaintext
📁 /log         # Automatically saved conversation logs
📁 /output      # Multiple-choice result summaries
📄 api_key.json # API access credentials
📄 agent_profile.xlsx  # Role descriptions and prompts
📄 [example] question_prompt.md  # Example question templates
📄 [example] scenario_prompt.md  # Example scenario templates
📄 [example] pic_test.jpg  # Example to test the fuction of scoring plans
