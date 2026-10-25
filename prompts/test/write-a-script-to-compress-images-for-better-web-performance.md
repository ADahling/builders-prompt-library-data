---
title: "Write a Script to Compress Images for Better Web Performance"
slug: write-a-script-to-compress-images-for-better-web-performance
stage: Test
category: "Cleanup & Warnings"
grade: A+
score: 92
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-a-script-to-compress-images-for-better-web-performance
---
# Write a Script to Compress Images for Better Web Performance

Get a shell script and guide for compressing website images, with adjustable quality, separate output files, and image format advice.

Variables: image_folder

## Prompt

I have a folder of high-resolution images (`{{image_folder}}`) that I want to use on my website. They are very large, and I know they will slow down my page load times. I want to compress them to reduce their file size without losing too much visual quality.

Your task is to provide a script and a workflow for compressing these images.

1.  **Image Compression Explained:** Briefly explain the difference between lossy and lossless compression. Why is image compression so important for web performance?
2.  **Tool Recommendation:** Recommend a command-line tool for image compression. `imagemin-cli` is a good choice for JPEGs and PNGs. For modern formats, `cwebp` for WebP is also a great option.
3.  **The Script:** Provide a shell script that iterates over all the images in the `{{image_folder}}` and uses the recommended tool to compress them. The script should:
    *   Take a quality setting as an argument.
    *   Save the compressed images to a new directory (e.g., `compressed/`) so that the original images are not overwritten.
4.  **Choosing the Right Format:** Briefly explain when to use JPEG, PNG, and WebP. (JPEG for photos, PNG for graphics with transparency, WebP for both).

Output should be a practical guide for a common web development task.

## Tips

Image optimization is one of the lowest-hanging fruits for improving web performance.
