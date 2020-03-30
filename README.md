# 1.1 Convolution
### 1

The equation to be used is:

(n-f+2p)/s + 1

64x111x111 -> 4x234x234

---------

x-dimension: 64 -> 4
n = 64, f = 61, p = 0, s = 1

(64-61+2(0))/1 + 1 = 3 + 1 = 4

---------

y-dimension: 111 -> 234

n = 111, f = 2, p = 62, s = 1

(111-2+2(62))/1 + 1 = 109+ 124 + 1 = 234

---------

z-dimension: same as y-dimension

### 2

256x56x56 -> 14x126x126

x-dimension: 256 -> 14

n = 256, f = 243, p = 0, s = 1

(256-243+2(0))/1 + 1 = 13 + 1 = 14

---------

y-dimension: 56 -> 126

n = 56, f = 3, p = 36, s = 1

(56-3+2(36))/1 + 1 = 53 + 72 + 1 = 126

---------

z-dimension: same as y-dimension

### 3

256x56x56 -> 42x72x72

x-dimension: 256 -> 42
n = 256, f = 215, p = 0, s = 1

(256-215+2(0))/1 + 1 = 41 + 1 = 42

---------

y-dimension: 56 -> 72
n = 56, f = 3, p = 9, s = 1

(56-3+2(9))/1 + 1 = 53 + 18 + 1 = 72

---------

z-dimension: same as y-dimension

# 1.2 Dropout
### a
torch.nn.functional.lp_pool2d(input, norm_type, kernel_size, stride=None, ceil_mode=False)
torch.nn.functional.avg_pool2d(input, kernel_size, stride=None, padding=0, ceil_mode=False, count_include_pad=True, divisor_override=None)
torch.nn.MaxPool2d(kernel_size, stride=None, padding=0, dilation=1, return_indices=False, ceil_mode=False)

### b
Max: Y_ij = max(S_ij)

Avg: Y_ij = avg(S_ij)

LP: Y_ij = (&sum; S_ij^p ) ^ 1/p

### c

| col1 | col2 |
| - | - |
| 109 | 92 |
| 110 | 85 |

### d
LP(p) = (&sum; x^p ) ^ 1/p

Max Pool = LP(infinity)

Avg Pool = LP(1)/n
