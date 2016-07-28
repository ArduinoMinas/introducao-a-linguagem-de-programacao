O C define através do arquivo de cabeçalho ```match.c``` um conjunto de funções para operações matemáticas bastante comuns no dia a dia dos programadores, em especial programadores para sistemas embarcados como os utilizados no Arduino.

Este capítulo é de referência, o ideal é que seja consultado sempre que precisar de uma função especifica da matemática, portanto deixeo sempre aberto quando iniciar seus estudos relativos a algortimos que demandem um maior uso de funções matemáticas.


## Functions

### Funções Trigonometricas
* cos
  Compute cosine (function )
* sin
  Compute sine (function )
* tan
  Compute tangent (function )
* acos
  Compute arc cosine (function )
* asin
  Compute arc sine (function )
* atan
  Compute arc tangent (function )
* atan2
  Compute arc tangent with two parameters (function )

### Funções Hiperbolicas
* cosh
  Compute hyperbolic cosine (function )
* sinh
  Compute hyperbolic sine (function )
* tanh
  Compute hyperbolic tangent (function )
* acosh 
  Compute area hyperbolic cosine (function )
* asinh 
  Compute area hyperbolic sine (function )
* atanh 
  Compute area hyperbolic tangent (function )

### Funções exponenciais e logaritimas
* exp
  Compute exponential function (function )
* frexp
  Get significand and exponent (function )
* ldexp
  Generate value from significand and exponent (function )
* log
  Compute natural logarithm (function )
* log10
  Compute common logarithm (function )
* modf
  Break into fractional and integral parts (function )
* exp2 
  Compute binary exponential function (function )
* expm1 
  Compute exponential minus one (function )
* ilogb 
  Integer binary logarithm (function )
* log1p 
  Compute logarithm plus one (function )
* log2 
  Compute binary logarithm (function )
* logb 
  Compute floating-point base logarithm (function )
* scalbn 
  Scale significand using floating-point base exponent (function )
* scalbln 
  Scale significand using floating-point base exponent (long) (function )

### Funções de potenciação
* pow
  Raise to power (function )
* sqrt
  Compute square root (function )
* cbrt 
  Compute cubic root (function )
* hypot 
  Compute hypotenuse (function )

### Funções de Erro  e gamma
* erf 
  Compute error function (function )
* erfc 
  Compute complementary error function (function )
* tgamma 
  Compute gamma function (function )
* lgamma 
  Compute log-gamma function (function )

### Funções de arredondamento e obtenção de resto
* ceil
  Round up value (function )
* floor
  Round down value (function )
* fmod
  Compute remainder of division (function )
* trunc 
  Truncate value (function )
* round 
  Round to nearest (function )
* lround 
  Round to nearest and cast to long integer (function )
* llround 
  Round to nearest and cast to long long integer (function )
* rint 
  Round to integral value (function )
* lrint 
  Round and cast to long integer (function )
* llrint 
  Round and cast to long long integer (function )
* nearbyint 
  Round to nearby integral value (function )
* remainder 
  Compute remainder (IEC 60559) (function )
* remquo 
  Compute remainder and quotient (function )

### Funções de manipulação de ponto flutuante
* copysign 
  Copy sign (function )
* nan 
  Generate quiet NaN (function )
* nextafter 
  Next representable value (function )
* nexttoward 
  Next representable value toward precise value (function )

### Funções para obtenção de Mínimo, Máximo e Diferença
* fdim 
  Positive difference (function )
* fmax 
  Maximum value (function )
* fmin 
  Minimum value (function )

## Outras Funções
* fabs
  Compute absolute value (function )
* abs
  Compute absolute value (function )
* fma 
  Multiply-add (function )

## Macros / Funções
Os recursos listados abaixo são implementados como macros no C e como funções no C++

### Classificação
* fpclassify 
  Classify floating-point value (macro/function )
* isfinite 
  Is finite value (macro )
* isinf 
  Is infinity (macro/function )
* isnan 
  Is Not-A-Number (macro/function )
* isnormal 
  Is normal (macro/function )
* signbit 
  Sign bit (macro/function )

### Comparação
* isgreater 
  Is greater (macro )
* isgreaterequal 
  Is greater or equal (macro )
* isless 
  Is less (macro )
* islessequal 
  Is less or equal (macro )
* islessgreater 
  Is less or greater (macro )
* isunordered 
  Is unordered (macro )

### Constantes Macros úteis

* math_errhandling 
  Error handling (macro )
* INFINITY 
  Infinity (constant )
* NAN
  Not-A-Number (constant )
* HUGE_VAL
  Huge value (constant )
* HUGE_VALF 
  Huge float value
* HUGE_VALL 
  Huge long double value (constant )

## Outras Macros
As macros abaixo foram definidas desde a versão C99 e C++11

| macro	| type	| description |
| --- |  --- |  --- | 
| MATH_ERRNO |
| MATH_ERREXCEPT	| int	| Bitmask value with the possible values math_errhandling can take. |
| FP_FAST_FMA |
| FP_FAST_FMAF |
| FP_FAST_FMAL	| int	| Each, if defined, identifies for which type fma is at least as efficient as x * y+z. | 
| FP_INFINITE |
| FP_NAN |
| FP_NORMAL | 
| FP_SUBNORMAL | 
| FP_ZERO	| int	| The possible values returned by fpclassify. |
| FP_ILOGB0 |
| FP_ILOGBNAN	| int	| Special values the ilogb function may return. |

## Tipos definidos para estas funções

* double_t 
  Floating-point type (type )
* float_t
  Floating-point type (type )



---

Revisado: {{ file.mtime }} | Compilado: {{ gitbook.time }}

---

Referência: http://www.cplusplus.com/reference/cmath/
