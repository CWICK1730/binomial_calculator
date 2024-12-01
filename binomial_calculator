import math
import streamlit as st

def binomial_probability(n, p, k):
    """
    Calculate the binomial probability of k successes in n trials 
    with success probability p.
    
    Args:
    - n: int, number of events
    - p: float, probability of success for each event (0 <= p <= 1)
    - k: int, number of successes
    
    Returns:
    - float, probability of exactly k successes
    """
    binomial_coeff = math.comb(n, k)
    probability = binomial_coeff * (p ** k) * ((1 - p) ** (n - k))
    return probability

# Streamlit App
st.title("Binomial Probability Calculator")

st.write(
    "This app calculates the probability of achieving a specific number of successes in a given number of trials using the binomial distribution."
)

# Input fields
n = st.number_input("Enter the number of events (n):", min_value=1, step=1, value=25)
p = st.slider("Enter the probability of success for each event (0 to 1):", 0.0, 1.0, 0.5)
k = st.number_input("Enter the number of successes (k):", min_value=0, step=1, value=3, max_value=n)

# Calculate probability
if st.button("Calculate"):
    result = binomial_probability(n, p, k)
    result_percentage = result * 100
    st.success(
        f"The probability of exactly {k} successes out of {n} trials is: {result_percentage:.6f}%"
    )
