# parcel-plugin-wasm.rs
wasm-bindgen support for Parcel bundler

### Requirements
* cargo
* wasm-pack

### Installation
```
npm i --save-dev parcel-plugin-wasm.rs
```

### Usage
```rust
extern crate wasm_bindgen;
use wasm_bindgen::prelude::*;

#[wasm_bindgen]
pub fn foo(x: &str) -> String {
  if x == "abc" {
    "yes".to_string()
  } else {
    "no".to_string()
  }
}
```

```javascript
import { foo } from 'path/to/Cargo.toml'

console.log(foo('abc'))    // yes
```
