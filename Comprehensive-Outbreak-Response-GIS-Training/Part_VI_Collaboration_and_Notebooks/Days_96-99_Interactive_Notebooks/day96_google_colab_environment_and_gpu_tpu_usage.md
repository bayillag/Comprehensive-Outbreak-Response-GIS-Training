# **Day 96 – Google Colab Environment & GPU/TPU Usage**  

Bloom Level: Apply & Create | Duration: 4 hrs  

## Objectives  

- Describe Google Colab architecture, notebook interface, and resource quotas.  

- Mount Google Drive and manage dependencies via `pip` and `conda` in Colab.  

- Enable and verify GPU and TPU runtimes, understanding their differences.  

- Leverage GPU acceleration for spatial computations (e.g., raster processing, matrix ops).  

- Utilize TPUs for TensorFlow‐based models and assess performance gains.  

- Profile and optimize code for execution within Colab’s hardware constraints.  

---

## Agenda  

1. Lecture: Colab Fundamentals & Hardware Accelerators (45 min)  
   - Colab environment, file system, and limits  
   - GPU vs. TPU architectures and use cases  

2. Demo: Notebook Setup & Resource Activation (30 min)  
   - Mounting Google Drive, installing libraries  
   - Switching runtime types and verifying via CUDA/TPU checks  

3. Lab Part 1 – GPU‐Accelerated Spatial Tasks (60 min)  
   - Load a sample raster dataset and perform convolution or zonal statistics with Numba/CuPy  
   - Compare CPU vs. GPU execution times for a matrix‐intensive operation  

4. Lab Part 2 – TPU for Machine Learning Models (45 min)  
   - Build and train a small TensorFlow model on TPU (e.g., classification of simulated health outcomes)  
   - Extract TPU logs and compare training speed to GPU  

5. Discussion & Q&A (30 min)  
   - Managing session timeouts and reconnects  
   - Best practices for data I/O and checkpointing  
   - Tips for extending Colab capacity (Drive mounting, session persistence)  

---

## Exercise Details  

**Data & Templates Provided:**  

- `day96_colab_template.ipynb`: starter notebook with sections for setup, GPU/TPU checks, and profiling.  
- `day96_sample_raster.tif`: medium‐size raster for parallel processing tests.  
- `day96_model_data.csv`: synthetic dataset for TensorFlow classification.  

**Key Tasks:**  

1. Open the provided notebook and mount your Google Drive.  
2. Install and import required packages (e.g., `rasterio`, `numba`, `cupy`, `tensorflow`).  
3. Switch to GPU runtime, load `day96_sample_raster.tif`, and execute a tiled convolution or zonal statistic in parallel; record execution time.  
4. Switch to TPU runtime, build a small TensorFlow model on `day96_model_data.csv`, train for 5–10 epochs, and log epoch times.  
5. Profile and document CPU, GPU, and TPU runtimes for both tasks, noting bottlenecks and memory constraints.  

---

## Assignment  

Submit to `assignments/day96/` by Day 97 morning:  

1. Colab Notebook  
   - `day96_colab.ipynb` with annotated code sections: setup, GPU task, TPU task, and profiling results.  

2. Performance Benchmark Table  
   - `day96_benchmarks.csv` listing task, runtime on CPU, GPU, and TPU, and memory usage.  

3. GPU‐Accelerated Script  
   - `day96_gpu_processing.py` extract from notebook demonstrating parallel raster operation.  

4. TPU Model Script  
   - `day96_tpu_model.py` showing model definition, TPU strategy setup, and training loop.  

5. Analytical Report (`day96_report.md`, 300 words)  
   - Discuss setup steps, performance comparisons, challenges in Colab’s environment, and recommendations for future tasks.  

6. Reflection (`day96_reflection.md`, 200 words)  
   - Reflect on your experience with Colab’s hardware accelerators, what surprised you, and how you’ll apply these skills in spatial epidemiology workflows.  

---

Harnessing Google Colab’s GPUs and TPUs will accelerate your spatial analyses and machine‐learning tasks—enabling scalable, reproducible experiments without local hardware constraints.
