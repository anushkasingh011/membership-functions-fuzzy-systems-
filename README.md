# membership-functions-fuzzy-systems-
A fuzzy set A in a universe of discourse X is characterized by a membership function μ_A(x) : X → [0, 1], which assigns to each element x ∈ X a degree of membership in A. 
Unlike classical (crisp) sets where membership is strictly binary (0 or 1), fuzzy sets allow partial membership — enabling the modeling of gradual, imprecise, or linguistic concepts such as 'tall', 'hot', or 'fast'. Key terminologies associated with a membership function are:
• Core: The region of the universe where μ_A(x) = 1 (full membership).
• Support: The region where μ_A(x) > 0 (any non-zero membership). 
• Crossover Points: Values of x where μ_A(x) = 0.5.
• Height: The maximum value of μ_A(x) across the universe (≤ 1). The five standard types of membership functions are:
• Triangular MF — defined by three parameters (a, b, c): rises linearly from a to b (peak), then falls to c. Simple and computationally efficient. 
• Trapezoidal MF — defined by four parameters (a, b, c, d): linear rise from a to b, flat top (full membership) from b to c, linear fall from c to d. 
• Gaussian MF — defined by mean (c) and standard deviation (σ): smooth symmetric bell curve. Differentiable, ideal for adaptive neuro-fuzzy systems. 
• Sigmoidal MF — defined by slope (a) and inflection point (c): monotonically increasing (or decreasing). Suitable for open-ended boundary conditions. 
• Generalized Bell MF — defined by width (a), slope (b), center (c): symmetric smooth bell with independently controllable width and slope. Mathematical Definitions: Triangular:    μ(x) = max( min( (x-a)/(b-a),  (c-x)/(c-b) ),  0 ) Trapezoidal:   μ(x) = max( min( (x-a)/(b-a),  1,  (d-x)/(d-c) ),  0 ) Gaussian:      μ(x) = exp( -( (x - c)² ) / ( 2σ² ) ) Sigmoidal:     Bell:          μ(x) = 1 / ( 1 + exp( -a(x - c) ) ) μ(x) = 1 / ( 1 + | (x - c) / a |^(2b) ) 
