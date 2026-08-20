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

  # CSAE The novelty
