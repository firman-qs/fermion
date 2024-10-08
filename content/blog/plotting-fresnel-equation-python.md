---
title: "Plotting Fresnel Equations with Python"
date: 2023-12-23T15:55:07+07:00
draft: false
math: true
authors:
  - name: firmanqs
tags:
  - Markdown
  - Example
  - Guide
description: "Nothing special, just XMonad rice"
---

## Simple Equation Derivation
We start with Fresnel Equations

\begin{equation}
\tilde{E}_{0_R} = \left(\frac{\alpha-\beta}{\alpha+\beta}\right)\tilde{E}_{0_I}, ~~~~~~ \tilde{E}_{0_T} = \left(\frac{2}{\alpha + \beta}\right) \tilde{E}_{0_I}. \tag{1}
\end{equation}


where

\begin{equation}
\alpha\equiv \frac{\cos\theta_T}{\cos\theta_I}, \tag{2}
\end{equation}

and

\begin{equation}
\beta \equiv \frac{\mu_1 v_1}{\mu_2 v_2} = \frac{\mu_1 n_2}{\mu_2 n_1}. \tag{3}
\end{equation}

If we assume the special case where \(\mu_1 \cong \mu_2 \cong \mu_0\) then

\begin{equation}
\beta \cong \frac{n_2}{n_1}. \tag{4}
\end{equation}

Based on Snell's law we know that

\begin{equation}
\sin\theta_T = \frac{n_1}{n_2} \sin\theta_I. \tag{5}
\end{equation}

Using identity \(\cos^2\theta_T+\sin^2\theta_T = 1\) then the previous \( \alpha \) equation (2) becomes

\begin{equation}
\alpha = \frac{\sqrt{1-\sin^2\theta_T}}{\cos\theta_I} = \frac{\sqrt{1-\left[(n_1/n_2)\sin\theta_I\right]^2}}{\cos\theta_I}.
\end{equation}

For reflectance and transmittance

\begin{equation}
\newcommand{\rbrak}[1]{\left(#1 \right)}
T\equiv\frac{I_T}{I_I}=\underbrace{\frac{\epsilon_2v_2}{\epsilon_1v_1}}_\beta\underbrace{\rbrak{\frac{E_{0_T}}{E_{0_I}}}}_\text{Eq. 1}\underbrace{\frac{\cos\theta_T}{\cos\theta_I}}_\alpha=\alpha\beta\rbrak{\frac{2}{\alpha+\beta}}^2.
\end{equation}


## Provided code
[[https://github.com/firman-qs/fresnel-equation-plot-python]]

## Final Result
{{< figure src="https://raw.githubusercontent.com/firman-qs/fresnel-equation-plot-python/main/Fresnel_equation_plot_python.png" alt="Fresnel Equations Plot">}}

## Video on Plotting Fresnel Equations
{{< youtube vb2NnQ_LcBE >}}
