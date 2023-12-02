# General Grant Proposal

* **Project:** implement liam-eagen-msm gadget in halo2 [#27](https://github.com/privacy-scaling-explorations/acceleration-program/issues/27)

## Project Overview :page_facing_up: 

### Overview

[Liam Eagen's paper](https://eprint.iacr.org/2022/596) suggested a protocol to prove a point on an elliptic curve is the multi-scalar multiplication of some points. We want to implement this on [halo2](https://github.com/privacy-scaling-explorations/halo2).

### Project Details 
Applying the protocol on a zk-SNARK will improve performance compared to directly proving the multiplication. The main idea of reducing proof size is to express the information of points on an element in the function field of the elliptic curve. The performance of this will depend on which proof system we use. To optimize, we want to first study about how zk-proof systems work, especially focusing on halo2 using [KZG](https://github.com/privacy-scaling-explorations/halo2) and [IPA](https://github.com/zcash/halo2). We will summarize about proof systems and materials in Liam Eagen's paper, and post it.

Next, we will implement the protocol using halo2, and compare the performance. The protocol can make the information of points or scalars zero-knowledge, or both. Each three versions can be optimized using the techniques described in the paper. The final output will be

* Implementation of the protocol using halo2.
* Summary about materials in elliptic curve inner product protocol.

## Team :busts_in_silhouette:

### Team members
* Names of team members: Seongsu Jeon
* Email: ssjeon@postech.ac.kr
* Telegram handle: @ssjeonp
* Discord handle: ssjeon


### Team Website	
* https://https://github.com/ssjeon-p

### Team's experience
PSE summer contribution 2023, learning about zkp and halo2.

Ph.D major in number theory and algebraic geometry (ongoing)

### Team Code Repos
* https://github.com/ssjeon-p


## Development Roadmap :nut_and_bolt: 

### Overview
* **Total Estimated Duration:** 8 weeks
* **Full-time equivalent (FTE):**  0.5
* Expected Start Date: Dec 11st 2023
* Expected End Date: Feb 11st 2024

### Milestone 1
* **Estimated Duration:** 2 weeks
* **FTE:**  0.5
* **Estimated delivery date**: Dec 24th 2023

#### Deliverables and Specifications
We want to study carefully about Liam Eagen's paper and some proof systems. We will focus on how the halo2 works and want to explore ways to optimize the ecip protocol if possible. The summary of what we studied will be posted on [blog.](https://ssjeon.blogspot.com/)

### Milestone 2
* **Estimated Duration:** 2 weeks
* **FTE:**  0.5
* **Estimated delivery date**: Jan 7th 2024

#### Deliverables and Specifications
We will first implement the simplest version of the ecip protocol. This doesn't require zero-knowledge setting. But, this needs some general functions and algorithms, for example calculating function field elements of an elliptic curve using incremental construction or Mumford representation. We will deliver test functions to check these.

### Milestone 3
* **Estimated Duration:** 4 weeks
* **FTE:**  0.5
* **Estimated delivery date**: Jan 11st 2024

#### Deliverables and Specifications
Now, we plan to make the protocol zero knowledge in scalars and points, and both. Each version needs some improvements using techniques in the paper. Plus, using elliptic curves with complex multiplication structure will reduce proof size so we want to explore this. After implementing every version of the protocol, we want to compare how this protocol improves performance compared to simply calculating multi-scalar multiplications on a circuit.
