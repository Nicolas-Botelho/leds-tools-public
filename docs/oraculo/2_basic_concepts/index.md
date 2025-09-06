---
sidebar_position: 1
title: Basic Concepts
---

# Basic Concepts

### Installation Prerequisites

- **Project Files**: Can be downloaded by zipfile or cloning the repository via git.

- **Docker**: All the containers are created with the needed technologies in the right environment via docker containers.

## How to Install

Follow these steps to run the project locally:

1. Clone the project to your local machine.

2. Generate a personal Github token and insert it on **GITHUB_TOKEN** in the `example.env` file.
    - Can be generated here: [https://github.com/settings/tokens](https://github.com/settings/tokens)

3. Generate a personal Gemini token and insert it on **GEMINI_API_KEY** in the `example.env`file.
    - Can be generated [https://aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey)

3. Rename the `example.env` file to `.env`

4. In the `main.py` file: Update the variable **repos** to your repositories, following the pattern. 
    - The repositories must be acessible through your given token.

5. While in the root of project, run the following commands to initiate the services.
    ps.: This, creating containers and setting up the environment inside the container, could take while

    To start the project:
    ```bash
      docker compose up -d
    ```

    To stop the project later, you can run:
    ```bash
      docker compose down
    ```

## How to use

After the **Open Web UI** container finishes setting up:

1. Go to Open web UI initial page: [http://localhost:3000/](http://localhost:3000/)
2. Create your local account. Dont worry, your email wont be verified
3. After logged in, go to [http://localhost:3000/admin/functions](http://localhost:3000/admin/functions)
4. In the **Functions** page, click on **import functions**
5. Select the file [**pipeline_api.json**](`src/assets/open_web_ui/pipeline_api.json`) in the `src/assets/open_web_ui/` folder
6. Activate the function through a slider on the top-right corner
7. Return to the initial page with [http://localhost:3000](localhost:3000)