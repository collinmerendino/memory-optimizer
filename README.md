# Server Memory Optimizer

A Python utility class for optimizing memory usage in server applications and data processing pipelines.

## Features
- Memory-efficient file streaming - Process large files line-by-line without loading into memory
- Object pooling - Reuse expensive objects like database connections
- Adaptive caching - Smart caching that auto-clears when memory is constrained
- Memory leak detection - Identify potential memory leaks in long-running processes
- Data offloading - Move large datasets to disk when memory limits are reached

---

## Prerequisites
- Python 3.7+
- numpy (for array offloading)
- psutil (for memory monitoring)

---

## Usage

1. Clone the repository:
```
git clone https://github.com/collinmerendino/memory-optimizer.git
pip install numpy psutil
cd memory-optimizer
```

2. Options:
```
.stream_large_file(file_path): Generator yielding file lines
.get_pooled_object(key, constructor): Get or create pooled object
.smart_cache(func): Decorator for adaptive caching
.check_memory_leak(threshold=1000): Detect potential leaks
.offload_to_sqlite(data, table_name): Store data in SQLite
.offload_to_memmap(array, file_path): Memory-map NumPy array
```

3. Run the program:
```
python3 memory.py
```

Contributing
Contributions are welcome! If you have suggestions for improvements, please open an issue or submit a pull request.

License
This project is licensed under the MIT License. 
