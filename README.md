# figure-out-the-coefficents-of-a-quadratic-equation.
AI related Math - figure out the coefficents of a quadratic equation.
def quadratic_function(a, b, c, x):
    return a * x * x + b * x + c
a = 1
b = 1
c = 1
learning_rate = 0.01
outputs = (2, 5, 7, 10)
for i in range(1000):
    a_losses = []
    b_losses = []
    c_losses = []
    for x, y in enumerate(outputs):
        guess = quadratic_function(a, b, c, x)
        a_losses.append(2 * (guess - y) * x * x)
        b_losses.append(2 * (guess - y) * x)
        c_losses.append(2 * (guess - y))
    a -= learning_rate * sum(a_losses) / len(a_losses)
    b -= learning_rate * sum(b_losses) / len(b_losses)
    c -= learning_rate * sum(c_losses) / len(c_losses)
print(a, b, c)
for input, output in enumerate(outputs):
    print(output, "=", quadratic_function(a, b, c, input))
a = round(a)
b = round(b)
c = round(c)
print(a, b, c)
for input, output in enumerate(outputs):
    print(output, "=", quadratic_function(a, b, c, input))
