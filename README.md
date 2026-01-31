# Lab-10-DIP
1.	Implement Huffman Coding.
2.	Implement JPEG-like DCT compression.
3.	Compute CR, MSE, PSNR,RD.
4.	Compare original vs compressed.
# Code Explanation
This code implements a JPEG-like image compression system using Discrete Cosine Transform (DCT) and Huffman coding. First, a grayscale (or color) image is uploaded in Google Colab and converted to grayscale and floating-point format for processing. The image is divided into 8×8 blocks, each block is level-shifted and transformed using the DCT to move pixel information into the frequency domain. These DCT coefficients are then quantized using a standard JPEG quantization matrix to remove less important high-frequency information, achieving compression. After quantization, the image is reconstructed by dequantization followed by inverse DCT, producing a compressed version of the original image. For entropy compression, Huffman coding is applied to the quantized coefficients by building a frequency-based Huffman tree and generating binary codes, which significantly reduces the number of bits required to store the image. Finally, the code evaluates compression performance by calculating Compression Ratio (CR), Mean Squared Error (MSE), Peak Signal-to-Noise Ratio (PSNR), and Rate-Distortion (RD), and displays both the original and compressed images for visual comparison.
