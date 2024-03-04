<h1>NukeDiffusion - Stable Diffusion for Nuke</h1> 

![NukeDiffusion_Cover_v002](https://github.com/danilodelucio/NukeDiffusion/assets/47226196/d230497e-f1d7-4687-9299-7f7487e5718f)

<br>**NukeDiffusion** is an integration tool for Nuke that uses [Stable Diffusion](https://stability.ai/) to generate AI images from prompts using local Checkpoints.
<br>It uses the official library from [Hugging Face](https://huggingface.co), and you don't need to create any account, everything works locally!

:white_check_mark: Unlimited image generation;
<br>✅ Local Checkpoints;
<br>✅ No internet connection required;
<br>✅ No sign in account required;
<br>✅ Free for non-commercial or commercial use;
<br>
<br>

> [!TIP]
> _You can use the [CivitAI](https://civitai.com/) website to download Checkpoints and try some different Prompts shared by the community._ 😉
<br>


Some limitations you need to consider for this first version:

📌 only for Windows (sorry 🐧 and 🍎);
<br>📌 generate single images only (not animation supported);
<br>📌 image files supported: **.jpg**, **.png**, **.tif** (does not support **.exr** and video files);
<br>📌 batch feature (multiple image generation) not included;

> [!NOTE]
> _For experienced users, **NukeDifussion** does not support ControlNet, Lora, AnimateDiff and other advanced controls, just the basic setup for image generation._
---
<h1>Workflows :briefcase:</h1>

For now, the included pipeline workflows are:

- **txt2img**: generates an image from a text description (which is also known as a Prompt);
- **img2img**: generates an image passing an initial image (user input) as a starting point for the diffusion process;
- **Inpainting**: replaces or edits specific areas of an image by a provided input mask.

---

<h1>NukeDiffusion node ☢️</h1>

The **NukeDiffusion** node is pretty straightforward. Everything you need is in the same panel, and the UI updates accordingly to your workflow option (**txt2img**, **img2img**, **inpainting**).

![NukeDiffusion_NodeUI_v002](https://github.com/danilodelucio/NukeDiffusion/assets/47226196/aa668518-cf08-4596-9539-9b1ceeb0f393)

---
<h1>NukeDiffusion Terminal 🤖</h1>

After clicking on the **Generate Button**, it will open the **NukeDiffusion Terminal**, which will load all the information provided in the **NukeDiffusion node**.


![Screenshot 2024-03-03 215656](https://github.com/danilodelucio/NukeDiffusion/assets/47226196/66c97762-9306-4d56-af24-d898053b97ef)

Here you don't have too much to do, just check the information and... wait! 😅

---

<details>
<summary><b>txt2img</b></summary>
 
</details>

<details>
<summary><b>img2img</b></summary>
 
</details>

<details>
<summary><b>inpainting</b></summary>
 
</details>

---
<h1>Installing</h1>
Here is the most annoying part... 😣 <br>
But don't give up, I'm sure you can do this! 🤓
<br>
Let me break it into a few parts:


---
<h1>Troubleshooting 🛠️</h1>

<details>
<summary><b>'triton' Error</b></summary>

The error `ModuleNotFoundError: No module named 'triton'` must be ignored!

Triton is a Open-source GPU programming for neural networks, and what I found regarding to this issue, is that Triton module is not available for Windows.
However, this error does not affect the image generation, so just simply ignore it!
 
 ![triton error](https://github.com/danilodelucio/NukeDiffusion/assets/47226196/06a3a408-681a-451a-8e1c-ce354e0a4e2d)

> _I didn't hide this issue so you can check on the Terminal if you get another import module error._
</details>

<details>
<summary><b>blank error message</b></summary>
 
 ![Screenshot 2024-03-03 200140](https://github.com/danilodelucio/NukeDiffusion/assets/47226196/cde41084-317a-47c5-9024-baba5ab5d5c7)

In **NukeDiffusion** node, when you click on **Refresh** button, it will load all the **Checkpoints** available in the directory you specified earlier on `checkpoints_path.json`, or if you are using the default path `./NukeDiffusion/models/checkpoints`.
If you open a Nuke script and see the `blank error message`, that is because the **Checkpoints pulldown choice menu** is trying to get the last checkpoint loaded in the previous session, which will raise an error.

For now, I suggest you to choose one of the 3 following options:

- delete the **NukeDiffusion** node before closing the Nuke script;
- leave the **Checkpoints pulldown choice menu** set to `Stable Diffusion [Default Model]`;
- simply ignore the error message, this will not affect your script at all.

> _Sorry for the inconvenience, I will fix it in the next release!_ 🙏

</details>

For any feedback, suggestions, bugs, or feature requests, please go to the [Issues](https://github.com/danilodelucio/NukeDiffusion/issues) page and create a **new issue**.



<h1>Support me! 🥺</h1>

![image](https://github.com/danilodelucio/NukeDiffusion/assets/47226196/ee1e5d16-43e2-46bc-bc48-aaf1d7559b87)

This personal project required a significant time and extra hours of hard work to make it available to everyone. <br>
It's not perfect and I still need to work in a lot of features, but for a first version I believe it can help Nuke users to live this experience. 🤖

If you find this tool useful, please consider supporting me on [Buy Me A Coffee](https://www.buymeacoffee.com/danilodelucio). :coffee: <br>
You can also share this tool or send me a positive message, it would help me in the same way.

If you believe in this project and want to sponsor it for future updates, reach out on my [Linkedin](https://www.linkedin.com/in/danilodelucio/).


<h1>Cheers! 🥂</h1>


