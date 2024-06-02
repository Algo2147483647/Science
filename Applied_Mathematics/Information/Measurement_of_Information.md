# Measurement of Information

[TOC]

## Measurement of Information

### Information Measurement of Event

#### Self-Information

- Define  
  
  If a sequence of symmetric functions $H_m(p1, p_2,..., p_m)$ satisfies the following properties:
  
  - Normalization: $H_2(1/2, 1/2) = 1$
  - Continuity: $H_2(p, 1 - p)$ is a continuous function of $p$
  - Grouping: $H_m(p_1, p_2,..., p_m) = H_{m-1}(p_1 + p_2, p_3, ..., p_m) + (p1 + p2) H_2(\frac{p_1}{p_1 + p_2},\frac{p_2}{p_1 + p_2})$ 
  
  prove that Hm must be of the form:
  
  $$
  I(x) = -\log \mathbb P(x)
  $$
  Before an event occurs, Uncertainty of event occurrence;   
  After an event occurs, the amount of information contained in the event, and the amount of information required to remove uncertainty.
  
- Include

  * Joint Self-Information
    - Define  
      $$
      I(x, y) = -\log \mathbb P(x, y)
      $$
      The amount of information provided after events $x, y$ occur simultaneously.

  * Conditional Self-Information
    - Define  
      $$
      I(x|y) = -\log \mathbb P(x|y)
      $$
      The amount of information that event x can provide when event y has occurred.

#### Mutual Information

- Define  
  $$
  I(x;y) = \log\frac{\mathbb P(x|y)}{\mathbb P(x)}
  $$
  The degree of statistical correlation between two random events $x, y$;   
  The amount of information about event $x$ that can be provided after event $y$ occurs;  
  Change of uncertainty of event $x$ after event $y$.

- Include

  * Conditional Mutual Information
    - Define  
      $$
      I(x;y|z) = -\log\frac{\mathbb P(x|y, z)}{\mathbb P(x|z)}
      $$

    - Property
      - $I(x;y) = I(x) - I(x|y)$  

### Information Measurement of Event Set 

#### Entropy, Average Self-Information

- Define  
  $$
  \begin{align*}
    H(X) &= \mathbb E_{\mathbb P(x)} (I(x))  \tag{Discrete Set}\\
      &= -\sum_x \mathbb P(x)\log \mathbb P(x)  \\
    h(X) &= -\mathbb E_{\mathbb P(x)}(\log \mathbb P(x)) \tag{Differential Entropy, Continuous set}\\
      &=-\int \mathbb P(x) \log \mathbb P(x) \mathrm d x
  \end{align*}
  $$

  For the Discrete set,  
  the average uncertainty of the information source;  
  the average amount of information provided by each source symbol;  
  the amount of information required to remove the average uncertainty of the information source  

- Property
  - Maximum entropy probability distribution
    - Maximum Entropy with limited amplitude
      $$
      h(X^N) ≤ \sum_{i=1}^N \log(b_i - a_i)
      $$
      The Maximum entropy probability distribution with limited amplitude is Uniform distribution.

    - Maximum Entropy with limited power
      $$
      h(X^N) ≤ \frac{N}{2} \log(2 \pi |\sigma |^{\frac{1}{N}})
      $$
      The Maximum entropy probability distribution with limited power is Gauss distribution. 

- Include
  * Joint Entropy 
    - Define  
      $$
      \begin{align*}
        H(XY) &= \mathbb E_{\mathbb P(xy)} (I(xy))   \tag{Discrete Set}\\
          &= -\sum_x \sum_y \mathbb P(xy) \log \mathbb P(xy)  \\
        h(x^N) &=-E_{\mathbb P(x)}(\log \mathbb P(x))   \tag{Continuous set}\\
          &=-\int_x \mathbb P(x) \log \mathbb P(x) \mathrm d x
      \end{align*}
      $$

  * Conditional Entropy 
    - Define  
      $$
      \begin{align*}
        H(Y|X) &= \mathbb E_{\mathbb P(xy)} (I(y|x))   \tag{Discrete Set}\\
          &= -\sum_x \sum_y \mathbb P(xy) \log \mathbb P(y|x)  \\
          &= \sum_x \mathbb P(x) H(Y|x)  \\
        h(X|Y) &=-E_{\mathbb P(xy)}(\log \mathbb P(x|y))  \tag{Continuous set}\\
          &=-\iint \mathbb P(xy) \log \mathbb P(x|y) \mathrm d x \mathrm d y
      \end{align*}
      $$

  * Cross Entropy
    - Define  
      $$
      \begin{align*}
        D(\mathbb P || \mathbb Q) &= \sum_x \mathbb P(x) \log \frac{\mathbb P(x)}{\mathbb Q(x)}  \tag{Discrete Set}\\
        D(\mathbb P || \mathbb Q) &= \int \mathbb P(x) \log \frac{\mathbb P(x)}{\mathbb Q(x)}\mathrm d x  \tag{Continuous set}
      \end{align*}
      $$

- Example 
  - Entropy of discrete time Gauss information source
      $$
      \begin{align*}
        h(X) &= \frac{1}{2} \log (2 \pi e \sigma ^2)  \tag{1D}\\
        h(X) &= \frac{1}{2} \log (2 \pi e \sigma ^2)  \tag{Multi-dim independence}\\
        h(x^N)&=\frac{N}{2} \log (2 \pi e |\sigma |^{\frac{1}{N}})  \tag{Multi-dim correlation}
      \end{align*}
      $$
    
    - Proof  
      1D:  
      $$
      \begin{align*}
        h(x) &= -E_{\mathbb P(x)} (\log \mathbb P(x))  \\
          &= -E_{\mathbb P(x)} (-\frac{1}{2} \log(2\pi \sigma ^2) - \log e · \frac{(x-\mu)^2}{2\sigma ^2})  \\
          &= \frac{1}{2} \log(2\pi \sigma ^2) + \log e · \frac{\mathbb E_{\mathbb P(x)} ((x-\mu)^2)}{2\sigma ^2}  \\
          &= \frac{1}{2} \log(2\pi \sigma ^2) + \log e · \frac{\sigma ^2}{2 \sigma ^2}  \\
          &= \frac{1}{2} \log(2\pi e \sigma ^2)
      \end{align*}
      $$

#### Average Mutual Information

- Define  
  $$
  \begin{align*}
    I(X;Y) &= \mathbb E_{\mathbb P(xy)} (I(x;y))   \tag{Discrete Set}\\
      &= \sum_{x,y} \mathbb P(xy) I(x;y)  \\
      &=\sum_{x, y} \mathbb P(x) \mathbb P(y|x) \log \frac{\mathbb P(y|x)}{\mathbb P(y)}  \\
    I(X;Y) &= Sup_{P, Q} I([X]_P ;[Y]_Q)  \tag{Continuous set}
  \end{align*}
  $$

#### Set-Event Mutual Information

- Define  
  $$
  I(X;Y) = \mathbb E_{\mathbb P(y|x)}(I(x;y)) = \sum_y \mathbb P(y|x) \log \frac{\mathbb P(y|x)}{\mathbb P(y)}
  $$

  The amount of information provided by event x about set Y.

#### Average Conditional Mutual Information

- Define  
  $$
  \begin{align*}
    I(X;Y|Z) &= \mathbb E_{\mathbb P(xyz)} (I(x;y|z))  \\
      &=\sum_{x,y,z} \mathbb P(xyz) \log \frac{\mathbb P(x|yz)}{\mathbb P(x|z)}
  \end{align*}
  $$

#### Mutual Information of Discrete Set & Continuous Set 

- Define 
  - Mutual Information of Discrete Set & Continuous Set 
    $$
    \begin{align*}
      I(X;Y) &= \log \frac{q(x|y)}{p(x)}  \\
        &= \log \frac{p(y|x)}{q(y)}
    \end{align*}
    $$

  - Average Mutual Information of Discrete Set & Continuous Set 
    $$
    \begin{align*}
      I(X;Y) &= \mathbb E_{p(x) p(y|x)}\left(\log \frac{p(y|x)}{q(y)}\right)  \\
        &= \sum_x p(x) \int p(y|x) \log \frac{p(y|x)}{q(y)}\mathrm d y
    \end{align*}
    $$

## Communication

### Channel

**Channel Capacity**

Channel Capacity is the theoretical maximum rate at which information can be reliably transmitted over a communication channel. Channel Capacity is given by the maximum of the mutual information between the input and output of the channel, where the maximization is with respect to the input distribution.
$$
C = \max_{\mathbb P(x)} I(X;Y)
$$
**Shannon–Hartley theorem**
$$
C = B \log_2(1 + \frac{S}{N})
$$

- $C$ is the channel capacity in bits per second, a theoretical upper bound on the net bit rate (information rate, sometimes denoted  $I$) excluding error-correction codes
- $B$ is the bandwidth of the channel in hertz (passband bandwidth in case of a bandpass signal)
- $\frac{S}{N}$ is the signal-to-noise ratio (SNR) or the carrier-to-noise ratio (CNR) of the communication signal to the noise and interference at the receiver (expressed as a linear power ratio, not as logarithmic decibels)

