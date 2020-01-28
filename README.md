## Create python module in rust with pyo3

 - only testing in ubuntu 18.04 LTS
 - reference : https://pyo3.rs/v0.9.0-alpha.1/#using-python-from-rust

## Build

```{bash}
cargo build --release
```

after building, just copy `librust_pyo3.so` in `./target/release` to `rust_pyo3.so` in `./`

```{bash}
cp ./target/release/librust_pyo3.so rust_pyo3.so
```


## Usage

 - In python or ipython,

```{python}
import rust_pyo3
rust_pyo3.sum_as_string(10, 20) # '30'
```

<br>