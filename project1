# Heapify function to maintain the heap property
def heapify(arr, n, i):
    largest = i  # Assume root is the largest
    left = 2 * i + 1  # Left child
    right = 2 * i + 2  # Right child

    # If left child is larger than root
    if left < n and arr[left] > arr[largest]:
        largest = left

    # If right child is larger than the largest so far
    if right < n and arr[right] > arr[largest]:
        largest = right

    # If the largest is not root
    if largest != i:
        arr[i], arr[largest] = arr[largest], arr[i]  # Swap
        heapify(arr, n, largest)  # Recursively heapify the affected subtree

# Heap-Sort algorithm
def heap_sort(arr):
    n = len(arr)

    # Build a max heap
    for i in range(n // 2 - 1, -1, -1):
        heapify(arr, n, i)

    # Extract elements from the heap
    for i in range(n - 1, 0, -1):
        arr[i], arr[0] = arr[0], arr[i]  # Swap
        heapify(arr, i, 0)  # Heapify the reduced heap

# Example usage
if name == "main":
    numbers = [12, 11, 13, 5, 6, 7]
    print("Original array:", numbers)
    heap_sort(numbers)
    print("Sorted array:", numbers)
