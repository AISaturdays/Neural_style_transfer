# Neural_style_transfer
An implementation of [neural style][paper] in TensorFlow. </br>
  ![](./image.jpeg) </br>
  
Presentation of [neural style][ppt].

Style transfer is the technique of recomposing images in the style of other images.
## Dependencies

    tensorflow
    matplotlib
    python 3
    
## Examples
  ![](./output/output1.jpg) </br>
  ![](./output/output2.jpg) </br>
  ![](./output/output3.jpg) </br>

## What does the paper do?
* Create artistic images of high perceptual quality.
* The key observation: the representations of content and style of an image in the Convolutional Neural Networks are separable.
* Use a pre-trained VGG-19 (average pooling) to ﬁnd another image simultaneously matches the content of a photograph and the style of a piece of art work.</br> </br>
   ![](./system_architecture.png)

## Loss
### Content representation and loss:
Given a chosen content layer l, the content loss is defined as the Mean Squared Error between the feature map F of our content image C and the feature map P of our generated image Y.   </br>

When this content-loss is minimized, it means that the mixed-image has feature activation in the given layers that are very similar to the activation of the content-image.

### Style representation and loss:
If the feature map is a matrix F, then each entry in the Gram matrix G can be given by: </br>

The loss function for style is quite similar to out content loss, except that we calculate the Mean Squared Error for the Gram-matrices instead of the raw tensor-outputs from the layers.  </br>

![](./loss.jpg)</br>








[paper]: http://arxiv.org/pdf/1508.06576v2.pdf
[ppt]: https://docs.google.com/presentation/d/1Rs_saCe34Qdvh1XzIGdLpRavNaartBZHIy3VcZCDTBs/edit?usp=sharing
