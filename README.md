# Minimize-Cost-for-Lamp-Purchase

In a vibrant marketplace, a man named Alex visits a shop that sells two types of magical lamps: green and yellow. The green lamp costs X rupees, and the yellow lamp costs Y rupees. Alex needs to buy exactly N lamps, but there's a catch - he must ensure that at least K of the lamps he buys are green.
Alex wants to spend the least amount of money possible while fulfilling this condition. Can you help Alex figure out the minimum amount he needs to pay to get the required lamps?

def minimize_cost(t, test_cases):

    results = []
    for case in test_cases:
        N, K, X, Y = case
        if X <= Y:
            cost = N * X
        else:
            cost = K * X + (N - K) * Y
        results.append(cost)
    return results

T = int(input().strip())
test_cases = [tuple(map(int, input().split())) for _ in range(T)]
results = minimize_cost(T, test_cases)
for result in results:
    print(result)
