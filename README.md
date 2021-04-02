# Food-Siamese-using-CLIP

<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAqsAAAIYCAYAAABKRaUqAAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADh0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uMy4yLjIsIGh0dHA6Ly9tYXRwbG90bGliLm9yZy+WH4yJAAAgAElEQVR4nOy9W6xly7nf9fuqxmXOudbqy77Z3tveji/Hdsw5zjknSEhBHE4ERFEeAoqEEiVEhFskEIIIIUAglMBDgAglQoKHwAMRSIjwFqFIAYGUcBKkXBz7cI59bMfe3t7X3t29e3f3Wmtexqiqj4eqGnPMucaYq1e7d++2e/ylteac41qjRn1V//puJarKhAkTJkyYMGHChAnPIswnXYAJEyZMmDBhwoQJE8YwkdUJEyZMmDBhwoQJzywmsjphwoQJEyZMmDDhmcVEVidMmDBhwoQJEyY8s5jI6oQJEyZMmDBhwoRnFhNZnTBhwoQJEyZMmPDMYiKrEz4RiMifEhH3pK8jIr8uIioin/1prz1hwoQJE7aY+u0JnxQmsvocQET+SuoI/sLe9s+m7b9+hWv9SyLyJJLz/lXgtWfoOhMmTJjwzGDqtydM2GIiq88P1sC/IyKf/6QLAqCqK1X94Fm5Th8iYkTEPslrTpgwYcJjYOq3HxFTv/3zjYmsPj/4f4HfBP78oYNE5Ksi8tdF5Cz9/e8i8uW079eB/zl91/T3Vw5c6z8WkTdEZCMid0Tk/xCRedq3bwb6UyLiROT3i8hvichKRP6miLwqIr8mIt8SkXMR+b9E5LX98w6UQUTkfxCRH6VrviEif15E6t4xf05Efigif1REvgc0wFcO1uaECRMmfPyY+u2p354AFJ90ASY8NSjw7wN/S0T+kqr+g/0DUof0fwI/BP7ptPm/Bv6GiHyd2HH+28B/C3wm7V8N3UxE/gjwHwF/gtjZvgD8+iVlNMCfBf51oCWaiv4q4IF/k6hl+F+Bvwj80cseOBcFuA38ceAD4BvAX07X/7O9414F/i3gXwY+At5/xOtPmDBhwseFqd+e+u0JTGT1uYKq/oaI/DViR/brA4f8ceBl4Peq6l0AEfljwJvAH1PV/0lEHqRr3brkdp8HbgF/Q1Vb4C3g25ecI8CfUdVvp3v/98BfAP5xVf1m2vaXgf/kkut0UNWwd/ybIvIlYgfX7/RmwJ9U1bce9doTJkyY8HFj6reBqd9+7jG5ATx/+A+Bf1JE/vDAvn8M+G7u8ACSX9H3076r4H8DSuAnEgMF/qSInFxyjgK/1fudO9b/b2/bi1fxTRKRf0NE/q6IfCAiZ8B/QeyU+/hg6vAmTJjwjGLqt6d++7nGRFafM6jqD4jmlP+Kj1GzrqrvAl8D/lWiOec/Bb4vIp87cFpQVd+/TLpWu7+NOJu/FCLyLwL/HdEs9YeAXwH+c2KH3Mf5o1xvwoQJE542pn576refd0xk9fnEf0b09fnTe9u/A3xdRF7KG0TkU8BXgd9Om5q0/dIZsqpuVPVvqOp/APwSsAD+hZ+++FfCrwHfUtW/qKrfVNV/BPyup1yGCRMmTPhpMfXbE55bTGT1OYSq3gH+S+DP7O36X4A7wF8VkV8Vkd9LdIx/lzjDBfhx+vzDIvKyiBwP3UNE/rVkxvk9EtOu/AngBPjuE36cy/B94JdE5J8XkS+JyL8L/JGnXIYJEyZM+Kkw9dtTv/08YyKrzy/+EnC3v0FVV8AfADbA/wP8LaKZ5Q+qapOO+fvAf0M0Sd0mRpgO4SPgXwH+JvA7wL8H/GlV/b+f9INcgr9MTNvyPwLfAv4J4M895TJMmDBhwpPA1G9PeC4hqk9iUYsJEyZMmDBhwoQJE548Js3qhAkTJkyYMGHChGcWE1mdMGHChAkTJkyY8MxiIqsTJkyYMGHChAkTnllMZHXChAkTJkyYMGHCM4uJrE6YMGHChAkTJkx4ZnFwJQwRmVIFTHiKMFhjEBEQIYSAqlJVFcYYNpsNqoo1w3OsoEoI4ep3NYacFWM3O4ayXXjl0TGUdzted+xaks57pMVd8hW50uFACAoI1lpMqkMNgRACYbR8n3wXMF4vAkisPRGk91dVFdZaHjz46Iq19LONsqguvLDHlYt+ve/KxdWvBYLIRbm9TC6uJhPwJOXCh0Bcon74Pp80LpUL2fYrIoIRoaprRGTnfRpjKMqSoihom4ZmsyGEgBiDtZbz89PR9mMG+uKnkWFIMXChPWleO4vRvlvyv/Sn+btJv7fXtBKQvWtod494uMR/+UdX193tDjRG1UBQN7hv7Dz1pDLvX2u4zlUCiGL61+t/74176RtjbTuflfdu77nX3g6Uv1+GfvuEKHOqSuuawZM/tmXbJkx42ngkIbniFY0R6AR5K6CHB4qBrSKYgcE6X/OTHvqGBp0thgeq/Y7544L3fqQzVsAQqQbdREZVWa1WT2XQ/FnAk5YLEYOw22Y/DrkIz8D7M2ZswacDg/pTkAtVxXt/6TF9AuFVWS7PUY3yLj2FgHQkTi/IzThh/yShHdG6sH3vvaSn2u7uvqR2p9LbEbrtOvKOM1fsqiwfrbGvynVuLiVsjInFILbc8NHlYlu81Ev2H3WvTqT/85OY4ouMvNOIiaxO+LmBiIxqXTlACE3S5OZjtgPvdhLadeB5JjpyLR3rQ/MFx/AYA/OTJGN58Bq4C4eIxtPA4fuY7pj+XwjhqZXvWcdjy0U+R3VnQvVYchEO6CJH3lOegDw6hqwjjw+BWG+jcjFOVp8GxieYw5pViHVjjKGsKowI3nvato3byhLnHG3bdkQ3WrSexYnffv0Pvw/p9u2fm1ibQiSoPW1rvx1dydilV+N4V71+PGlw63ayMXT89nllb58mTbSkz0/8LR+QnYmsTvi5gYhQz2aDg8WoWSWZSPfdALJ5MmsVLrgJ6EUNBOxNXPfuEzUhQ3uv6gaw7WSujuF7HDYTH9CsPkYJroQ0YA7XzXZQ7v8BWGspiql7AzDWUtf14L6ryMX2eyBr4DqTcs+UN3wjBpvrZXJxVeJ32K1gDCN1APhRuRi/z6UatScBiW4LIzsZk4tMSuu6xhiD857NZkNRFCwWC5qmYb1aEUKI7gFFQdtuLtXiPn0ocLFMknftGa1l5wD2lANZy5pJXd/9Zfjug2OMMTvvftyNZntfHXiG8eOJ6s+hfTI68kQiKrkeBJGtUmZH67xz/rM30Z968wk/VxgT8v7Au48hs13UzvkREsslnfeYxmNU78TVO4cnOweOZPVQ+T45PIrPqiQtU9aSP46P5s8znoRcZGLa/9u59kHf2EM2z09anzMufyGMyfl4mZ9WyxvvgwbIai5b0qyulsvYx6ninEOAs9PT7RXSe98k/9VnDTKmlJRhyjX8tvpb8zNu26mOtFlJ98ifu76r+Rh5BLI6ggPHKmHkwXWYQKtisttCR2glufFo+tX3VyX6Aw9ivzbHCPLj49DkdCKrE55NPI5ZHEbNv9mkdfE2uuMTOaZZ7ZepP1APYUjeopXm6sk3Pk7zm0g/fODZJKpwqA6iRkQBSe89Kpx7Gr8JnZZ0CGNyEUK4IBfb+twjuOl7uFQuxtxJnh256Aj5x3L1J4vL6iBrvnNwVUYIgTaErTZcFTEmBlruTV5ifXw85R8q7z767gt9GC6qBKK2cOfsnuE7acI179n+3/qm7pOvPc11Lkv6H9Lx2YNbg+6cbnrHD8mfCIgZqdzRgKlYzAv1IYly7vl9GhF2A7KkO2T/FppvMPDOd2V3W6fRqHJRrvfLN3ZMv5++rM+eyOqEZwYiEjVklwx6o1ClbdvRfQdu3B3TDc5p83406OUYMV0eCro4MDg+nlnzMKRnQgwhXOKpJKNuRE/LN2800jUPPBI7ZWMMJkV0578J0TTfNM3IzlE7587+Cz6rV2yTY0FHnb/4SNkGDZsfk0zkNrPvAjFyxs+GXPRkwaTo/lznfSJYFAXGWrxzOOcIQbvzz84epowJT/9Z4nMMk5iLej5B+9pMzE4zkUQvsyY0H+o7q1Kv798tXXeFoii6SVx2ecn67ajB3tap3yvzvrldFf"/>
