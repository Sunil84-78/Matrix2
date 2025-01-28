def rotate_matrix(matrix):
    n = len(matrix)
    for i in range(n):
        for j in range(i, n):
            matrix[i][j], matrix[j][i] = matrix[j][i], matrix[i][j]
    for i in range(n):
        matrix[i].reverse()
def print_matrix(matrix):
    for row in matrix:
        print(row)
def input_matrix():
    n = int(input("Enter the size of the matrix (n x n): "))
    matrix = []
    print("Enter the elements of the matrix row by row:")
    for i in range(n):
        row = list(map(int, input(f"Enter row {i + 1}: ").split()))
        matrix.append(row)
    return matrix
matrix = input_matrix()
print("\nOriginal Matrix:")
print_matrix(matrix)
rotate_matrix(matrix)
print("\nMatrix after 90 degree rotation:")
print_matrix(matrix)
