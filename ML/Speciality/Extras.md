## Exploratory Data Analysis

- [The Shape of Data: Distributions: Crash Course Statistics #7](https://www.youtube.com/watch?v=bPFNxD3Yg6U)
- Normal distribution:
```
Let's understand the complete normal distribution formula:

(1/(σ√(2π))) * e^(-(x-μ)²/(2σ²))

1. It has TWO main parts:
   - (1/(σ√(2π))) : The normalizing constant
   - e^(-(x-μ)²/(2σ²)) : The exponential part that gives the bell shape

2. What each part does:
   - Normalizing constant ensures total area = 1 (100% probability)
   - Exponential part creates the bell shape
   - Together they make a perfect probability distribution

3. How parameters affect the shape:
   μ (mean):
   - Controls where the peak is
   - Shifts the curve left or right
   
   σ (standard deviation):
   - Controls the spread/width
   - Larger σ = flatter, wider curve
   - Smaller σ = taller, narrower curve

4. Key properties that result:
   - Symmetric around the mean
   - 68% of data within ±1σ
   - 95% within ±2σ
   - 99.7% within ±3σ

    For 68% (±1σ): ∫(from μ-σ to μ+σ) (1/(σ√(2π))) * e^(-(x-μ)²/(2σ²)) dx ≈ 0.6826 (68.26%)
    For 95% (±2σ): ∫(from μ-2σ to μ+2σ) (1/(σ√(2π))) * e^(-(x-μ)²/(2σ²)) dx ≈ 0.9544 (95.44%)
    For 99.7% (±3σ): ∫(from μ-3σ to μ+3σ) (1/(σ√(2π))) * e^(-(x-μ)²/(2σ²)) dx ≈ 0.9973 (99.73%)

5. Example:
   For height of adult males:
   - If μ = 5'10" (mean height)
   - σ = 3 inches (standard deviation)
   Then:
   - 68% are between 5'7" and 6'1"
   - 95% are between 5'4" and 6'4"
   - 99.7% are between 5'1" and 6'7"

The beauty of this formula is that it describes many natural phenomena and is foundational in statistics and probability theory.
```
