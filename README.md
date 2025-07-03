# NEURAL-STYLE-TRANSFER

*COMPANY*:CODTECH IT SOLUTIONS

*NAME*:LISBON RAJA B

*INTERN ID*:CT04DG3488

*DOMAIN*:WEB DEVELOPMENT

*DURATION*:4 WEEKS

*MENTOR*:NEELA SANTOSH

*DESCRIPTION*:
              This Python script implements a neural style transfer model using PyTorch to blend the artistic style of one image with the content of another, producing a new image that maintains the spatial structure of the content image but adopts the visual appearance of the style image. The script starts by setting up the computing device, allowing it to utilize GPU acceleration if available, which significantly speeds up the processing of high-resolution images. Images are loaded and preprocessed with resizing and normalization steps, ensuring they match the input requirements of the pre-trained VGG19 convolutional neural network used as the feature extractor. The script includes utility functions for loading images and displaying intermediate and final results with Matplotlib. It defines custom PyTorch modules for computing content and style losses: ContentLoss measures the mean squared error between the features of the content image and the generated image at a chosen convolutional layer, preserving the semantic information of the content; StyleLoss computes the difference between the Gram matrices of the style image and the generated image, capturing the textures and patterns characteristic of the artistic style. The model construction function, get_style_model_and_losses(), builds a new network by iterating through layers of the pre-trained VGG19 and inserting the normalization layer, content loss layers, and style loss layers at appropriate points. This approach allows the model to accumulate style and content losses during forward passes, which are then used to optimize the generated image. The script uses the L-BFGS optimizer, known for its effectiveness in optimizing image data for style transfer, to iteratively adjust the pixels of the input image so that the total loss—composed of weighted style and content losses—is minimized. The optimization process clamps the pixel values to the valid range [0,1] after each update to ensure the image remains visually plausible. Detailed progress logging is implemented, printing the current style and content loss values every 50 steps to give insight into the convergence of the algorithm. After completing the optimization, the final stylized image is saved to disk as styled_output.jpg and displayed to the user. The script handles potential mismatches in image sizes and supports dynamic adjustment of content and style weight hyperparameters, enabling fine control over the balance between content preservation and style application. The code is modular, making it easy to adapt or extend for other experiments,such as using different layers for losses, incorporating alternative normalization schemes, or applying additional regularizations. This implementation provides a complete, practical example of neural style transfer as introduced by Gatys et al., highlighting the power of convolutional neural networks in capturing perceptual features of images. It is suitable for students, researchers, or developers who want to explore deep learning-based artistic applications or integrate style transfer capabilities into creative tools. Clear comments and structure make it accessible even to beginners familiar with Python and PyTorch. Overall, this script demonstrates how deep neural networks can achieve impressive artistic effects by separating and recombining content and style representations of images, opening doors to innovative uses in digital art, design, and multimedia.

*OUTPUT*:

![Image](https://github.com/user-attachments/assets/95247292-e684-4495-b47a-120cde7c2021)
