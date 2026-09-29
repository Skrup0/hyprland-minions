The eyes require imgborders with a patch that renders them in the center of the top edge.
To apply the patch, make sure you've got the Hyprland headers for the Hyprland version you're running.

### 1. Clone imgborders

```sh
git clone https://codeberg.org/zacoons/imgborders ~/Documents/imgborders
cd ~/Documents/imgborders
```

### 2. Apply the patch

```sh
git apply imgborders.patch
```

### 3. Build

```sh
cmake -B build
cmake --build build -j$(nproc)
```

### 4. Load it

```sh
hyprctl plugin load ~/Documents/imgborders/build/libimgborders.so
```
