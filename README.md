# rolling-of-two-dice-10-000-times.
Simulate the rolling of two dice 10,000 times. • Estimate the probability of getting a sum of 7. • Compare it with the theoretical probability calculated mathematically.
import random

# Number of simulations
n = 10000

# Counter for how many times the sum is 7
count_sum_7 = 0

# Simulate rolling two dice n times
for _ in range(n):
    die1 = random.randint(1, 6)
    die2 = random.randint(1, 6)
    total = die1 + die2
    if total == 7:
        count_sum_7 += 1

# Experimental probability
experimental_prob = count_sum_7 / n

# Theoretical probability
# Total possible outcomes = 6 × 6 = 36
# Favourable outcomes for sum = 7 → (1,6),(2,5),(3,4),(4,3),(5,2),(6,1) → 6 ways
theoretical_prob = 6 / 36

# Display results
print("🎲 Dice Rolling Simulation (10,000 rolls)")
print("--------------------------------------")
print(f"Number of times sum = 7: {count_sum_7}")
print(f"Experimental Probability = {experimental_prob:.4f}")
print(f"Theoretical Probability  = {theoretical_prob:.4f}")
print(f"Difference = {abs(experimental_prob - theoretical_prob):.4f}")

🎲 Dice Rolling Simulation (10,000 rolls)
--------------------------------------
Number of times sum = 7: 1654
Experimental Probability = 0.1654
Theoretical Probability  = 0.1667
Difference = 0.0013
