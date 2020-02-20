This is a CMake wrapper for [skarupke/flat_hash_map](https://github.com/skarupke/flat_hash_map).

## Usage
Make this repository a submodule of your project. Then add in your CMakeLists.txt:

```
# add the path to this project
add_subdirectory(skarupke)

# ...

target_link_libraries(your-target PUBLIC skarupke::flat_hash_map)
```
