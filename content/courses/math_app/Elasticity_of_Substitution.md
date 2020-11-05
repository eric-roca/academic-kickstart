---
title: Elasticity of substitution
linktitle: Elasticity of substitution
toc: true
type: docs
date: "2019-07-11T00:00:00Z"
lastmod: "2019-07-11T00:00:00Z"
draft: false
menu:
  math_app:
    parent: Appendix
    weight: 4 

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 4
---

The elasticity of substitution between two inputs of a production function (or two goods in a utility function) measures _the percentage change in the ratio of the two inputs relative to the percentage change in their prices_.

The elasticity of substitution represents the curvature of the isoquant, this is, the degree of substitutability between inputs.
Mathematically, for inputs $x\_{1}$ and $x\_{2}$ and a production function $f(x\_{1}, x\_{2}),$ it is defined as:

$$\sigma\_{1,2} = - \frac{\partial \frac{x\_{1}}{x\_{2}}}{\partial \frac{p\_{1}}{p\_{2}}} \frac{\frac{p\_{1}}{p\_{2}}}{\frac{x\_{1}}{x\_{2}}}.$$

Assuming perfect competition, factor prices equal their margial product: $p\_{1} = \frac{\partial f(x\_{1},x\_{2})}{\partial x\_{1}}.$
Hence:

$$\sigma\_{1,2} = 
\textcolor{orange}{\boldsymbol{-}} \frac{ \partial \frac{x\_{1}}{x\_{2}}}
	{\partial \frac{ \frac{\partial f(x\_{1},x\_{2})}{\partial x\_{1}}}{\frac{ \partial f(x\_{1},x\_{2})}{\partial x\_{2}}}}  
\frac{ \frac{ \frac{ \partial f(x\_{1},x\_{2})}{\partial x\_{1}}}{ \frac{ \partial f(x\_{1},x\_{2})}{\partial x\_{2}}}}
	{ \frac{x\_{1}}{x\_{2}}} = 
\textcolor{orange}{\boldsymbol{-}} \frac{ \partial \ln \left( \frac{x\_1}{x\_2} \right)}
	{\partial \ln \left( \frac{ \frac{\partial f(x\_1,x\_2)}{\color{red}{\partial x\_1}}}{\frac{ \partial f(x\_1, x\_2)}{\color{green}{\partial x\_2}}} \right)} = 
 \frac{ \partial \ln \left( \frac{x\_1}{x\_2} \right)}
	{\partial \ln \left( \frac{ \frac{\partial f(x\_1,x\_2)}{ \color{green}{\partial x\_2}}}{\frac{ \partial f(x\_1, x\_2)}{\color{red}{\partial x\_1}}} \right)} 
$$

## Cobb-Douglas example

The Cobb-Douglas production function has an elasticity of substitution equal to one.

$$\begin{eqnarray}
& F(K,L)= A K^\alpha L^{1-\alpha}, \\\\\\
& w = A(1-\alpha) K^\alpha L^{-\alpha}, \\\\\\
& r = A \alpha K^{\alpha-1} L^{1-\alpha}.\end{eqnarray}$$
Hence:
$$\frac{w}{r} = \frac{1-\alpha}{\alpha} \frac{K}{L}.$$
Therefore, we can compute $\sigma\_{K,L}$ as

$$\frac{ \partial \ln \left(\frac{K}{L}\right)}{\partial \ln \left(\frac{w}{r}\right)} = 
	\frac{\color{red}{\partial \left( \frac{K}{L} \right)}}{\color{green}{\frac{K}{L}}} \frac{\frac{w}{r}}{\color{red}{\partial \frac{w}{r}}} = 
	\color{red}{\underbrace{\frac{\alpha}{1-\alpha}}\_{\frac{\partial \left( \frac{K}{L} \right)}{\partial \frac{w}{r}}}}  \color{green}{\underbrace{\frac{1-\alpha}{\alpha}\frac{K}{L}}\_{\left(\frac{w}{r}\right)}}\frac{L}{K}=1$$

## CES function

In the case of a CES function, the elasticity of substitution equals $\frac{1}{1-\rho}.$

$$\begin{eqnarray}
& F(K,L)= A \left( \alpha K^{\rho} + (1-\alpha) L^{\rho} \right)^\frac{\nu}{\rho}, \rho \leq 1 \\\\\\
& w = A \frac{\nu}{\rho}\left( \alpha K^{\rho} + (1-\alpha) L^{\rho}\right)^{\frac{\nu}{\rho}-1} ( 1- \alpha) \rho L^{\rho-1}, \\\\\\ 
& r = A \frac{\nu}{\rho}\left( \alpha K^{\rho} + (1-\alpha) L^{\rho} \right)^{\frac{\nu}{\rho}-1}\alpha \rho K^{\rho-1}.\end{eqnarray}$$
Hence:
$$\frac{w}{r} = \frac{1-\alpha}{\alpha} \left(\frac{K}{L} \right)^{1-\rho}.$$

The parameter $\nu$ indicates the degree of [homogeneity of the function.]({{< ref "Homogenous_Functions.md" >}})

The elasticity of substitution equals:

$$\frac{ \partial \ln \left(\frac{K}{L}\right)}{\partial \ln \left( \frac{w}{r} \right)} = 
	\frac{ \partial \frac{K}{L}}{\frac{K}{L}}\frac{\frac{w}{r}}{\partial \frac{w}{r}} = 
	\frac{\alpha}{1-\alpha}\frac{1}{1-\rho}\left(\frac{w}{r}\frac{\alpha}{1-\alpha}\right)^{\frac{1}{1-\rho}-1}
	\frac{1-\alpha}{\alpha}\left(\frac{K}{L}\right)^{1-\rho}\frac{L}{K} = 
	\frac{1}{1-\rho}.$$
