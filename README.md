# 🖼️ Watermark Embedder for Grayscale BMP Images

This is a simple C++ project for embedding a watermark (logo) onto a grayscale BMP image.  
The program blends the watermark with the original image using pixel-level averaging and saves the result as a new BMP file.

## 📁 Project Files

- `watermark.cpp` - Main C++ source file
- `AIgened_gray.bmp` - Grayscale input image
- `logo.bmp` - Grayscale watermark image
- `xxx.bmp` - Output image with watermark applied

## 🧠 How It Works

1. Reads the BMP file headers and extracts image dimensions.
2. Loads pixel data into 2D vectors.
3. For each pixel in the watermark:
   - If the pixel intensity is less than 250, blend it with the corresponding pixel in the main image:
     ```
     blended_pixel = 0.5 * watermark_pixel + 0.5 * image_pixel
     ```
4. Writes the new image to `xxx.bmp` with the correct BMP header.

## ⚠️ Notes

- The program only supports 8-bit grayscale BMP files (no compression).
- The watermark is applied starting from the top-left corner.
- Output is saved as `xxx.bmp` (overwrite warning).

## 📷 Example

**Input Images:**

- 🖼️ `AIgened_gray.bmp`
- 🔖 `logo.bmp`

**Output Image:**

- ✅ `xxx.bmp` (Watermarked)

