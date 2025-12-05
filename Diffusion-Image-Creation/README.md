# 🎨 Image Generation with Diffusion Models

This project explores how modern diffusion models can generate high‑quality images from random noise by iteratively denoising latent representations. The notebook walks through the full process of loading a pre‑trained diffusion pipeline, configuring generation parameters, and producing custom images programmatically.

---

## 📌 Objectives

- Understand the high‑level idea behind diffusion models for image synthesis  
- Use a pre‑trained diffusion pipeline to generate images from noise  
- Experiment with core hyperparameters such as guidance scale, number of inference steps, and image size  
- Save and visualize generated outputs for comparison and analysis  

---

## 🧰 Technologies & Libraries

- **Python** – main language for experimentation  
- **Diffusion / Generative Model Library** (e.g., Hugging Face Diffusers or similar) – pre‑trained image generation pipeline  
- **PyTorch** – tensor operations and model execution (if used by the pipeline)  
- **Matplotlib** – displaying generated images  
- **NumPy** – basic numerical utilities  

*(Adjust this list to match exactly what is imported in your notebook.)*

---

## 🔍 What the Notebook Does

### 1️⃣ Load and Configure the Diffusion Pipeline

- Loads a pre‑trained diffusion model capable of image synthesis  
- Sets device configuration (CPU or GPU)  
- Defines default parameters such as:
  - Number of inference steps  
  - Guidance scale / conditioning strength  
  - Output image resolution  

### 2️⃣ Generate Images from Noise

- Starts from random noise in latent space  
- Runs the denoising process step by step through the diffusion pipeline  
- Produces one or more final images for a given configuration  
- Optionally supports different seeds to make runs reproducible  

### 3️⃣ Visualize and Save Results

- Renders generated images inline in the notebook for quick inspection  
- Optionally saves results to disk (e.g., `results/` folder) with timestamped filenames  
- Encourages side‑by‑side comparison when varying parameters  

---

## 🧪 Experiments & Observations

Examples of experiments performed:

- Changing the number of inference steps to see its effect on image quality and detail  
- Adjusting guidance scale (if using text guidance) to trade off creativity vs. adherence to prompts  
- Running the same configuration with different random seeds to compare variation in outputs  

Key takeaways:

- More diffusion steps generally improve detail up to a point, but increase compute time  
- Guidance strength helps balance realism and prompt fidelity when conditioning is used  
- Random seeds strongly influence specific image outcomes even with identical settings  

---

## 📘 Learning Outcomes

From this lab you learn:

- How diffusion models progressively denoise random noise into coherent images  
- How to work with a pre‑trained generative pipeline in Python  
- How hyperparameters influence the visual quality and diversity of generated images  
- How to structure a simple experimentation loop for generative models (configure → generate → visualize → compare)  

---

## ▶️ How to Run

1. Open the notebook `Image Creation with Diffusion.ipynb` in Jupyter or Google Colab.  
2. Install required libraries (see the first cell or `requirements.txt` if provided).  
3. Run cells in order:
   - Environment setup  
   - Model / pipeline loading  
   - Image generation cells  
   - Visualization / saving cells  
4. Check the `results/` or output cells for generated images.


