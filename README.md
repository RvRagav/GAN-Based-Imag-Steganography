# GAN-Based Image Steganography

This project implements a deep learning-based steganography system using Generative Adversarial Networks (GANs) to securely embed sensitive medical data into grayscale images. The system focuses on robust, high-capacity, and imperceptible data hiding, with applications in medical privacy and security.

---

## Features

- **GAN-based Steganography**: Generator embeds binary medical data into cover images; extractor recovers hidden data.
- **Medical Data Simulation**: Uses the [Faker](https://faker.readthedocs.io/) library to generate realistic patient information.
- **Error Correction**: Integrates Reed-Solomon encoding for improved message recovery.
- **Robustness Evaluation**: Includes PSNR/SSIM metrics and attack simulations (e.g., JPEG compression, Gaussian noise).
- **Steganalysis**: CNN-based classifier distinguishes between cover and stego images.
- **Streamlit GUI**: User-friendly web interface for embedding, extracting, and visualizing results.

---

## Project Structure

- `Testing.ipynb`: Main notebook for data generation, model evaluation, and robustness testing.
- `Gan_new_training1.ipynb`: GAN training, message encoding, and evaluation.
- `GUI.ipynb`: Streamlit interface prototyping.
- `app.py`: Streamlit application for end-to-end demo.
- `Saved_Models/`: Trained generator, discriminator, and extractor models.
- `README.md`: Project documentation.

---

## Key Technologies

- Python, NumPy, TensorFlow/Keras
- Streamlit (GUI)
- Faker (synthetic data)
- ReedSolomon (error correction)
- scikit-image (metrics)
- Matplotlib (visualization)

---

## Usage

### 1. Install Dependencies

```bash
pip install streamlit faker keras reedsolo scikit-image matplotlib
```

### 2. Run the Streamlit App

```bash
streamlit run app.py
```

### 3. Notebooks

- Use `Testing.ipynb` and `Gan_new_training1.ipynb` for experiments, training, and evaluation.

---

## Example Workflow

1. **Generate Patient Data**: Synthetic binary messages are created using Faker.
2. **Encode with Reed-Solomon**: Messages are encoded for error correction.
3. **Embed in Image**: The generator model hides the message in a cover image.
4. **Extract & Decode**: The extractor recovers the message, which is then decoded and compared to the original.
5. **Evaluate**: PSNR/SSIM and bit error rate (BER) are computed. Steganalysis model can classify images as cover or stego.

---

## References

- [Faker Documentation](https://faker.readthedocs.io/)
- [Streamlit Documentation](https://docs.streamlit.io/)
- [ReedSolomon](https://pypi.org/project/reedsolo/)
- [Keras](https://keras.io/)

---

## License

This project is for academic and research purposes only.
