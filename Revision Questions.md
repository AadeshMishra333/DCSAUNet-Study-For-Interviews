# PFC
- Why is the first layer 3×3 and not 7×7?
- What is a depthwise convolution?
- Why is depthwise more efficient than standard convolution?
- Why is a 1×1 convolution needed after depthwise?
- Why does the block end with residual addition?
- What feature-extraction advantage does PFCBlock provide compared to a simple Conv-BN-ReLU stem?

# CSA
- Why split channels into two branches?
- Why is f2 = f2 + f1 used?
- Why apply Global Average Pooling?
- Why use Softmax instead of directly adding the branches?
- Why is residual addition still needed after attention?

# ESE
- Why is standard SE insufficient for segmentation?
- What is the difference between cSE and sSE?
- Why is a 1×1 convolution used after concatenation?
- Why add the refined feature back to the input through a residual connection?
- Why might ESE be more useful in the decoder than the encoder?

# 30 Seconds Architecture Overview

> The network follows an encoder-decoder structure. The PFCBlock first extracts multi-scale low-level features using standard, depthwise and pointwise convolutions with residual learning. Three CSABlock encoder stages progressively increase contextual understanding while reducing spatial resolution through max pooling. At the bottleneck, the network captures high-level semantic information. During decoding, bilinear upsampling and skip connections progressively restore resolution. Each decoder stage employs CSABlock_ESE, where CSA performs feature selection between branch representations and ESE refines channel-wise and spatial importance. Finally, a 1×1 convolution produces pixel-level logits that are converted to segmentation probabilities using a sigmoid function during inference
