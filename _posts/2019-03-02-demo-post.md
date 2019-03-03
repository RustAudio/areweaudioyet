---
layout: post
title: "First demo post"
date: 2019-03-02 17:44:05 -0800
---

Hey, this is just demo content, okay?

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam sed faucibus neque, fringilla rutrum orci. Nullam a urna in velit tristique bibendum eu sed leo. Nulla efficitur sollicitudin mollis. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Nulla fermentum lacinia magna nec efficitur. Phasellus varius, ex ut mattis lacinia, magna ex gravida ex, eget blandit odio urna ac nisl. Ut lobortis auctor nisl sit amet aliquam. Nullam luctus vulputate arcu, sed faucibus risus porttitor quis.

Example borrowed from [Rust VST Readme](https://github.com/rust-dsp/rust-vst):

## Example Plugin

A simple plugin that bears no functionality. The provided Cargo.toml has a
crate-type directive which builds a dynamic library, usable by any VST host.

`src/lib.rs`

```rust
#[macro_use]
extern crate vst;

use vst::plugin::{Info, Plugin};

#[derive(Default)]
struct BasicPlugin;

impl Plugin for BasicPlugin {
    fn get_info(&self) -> Info {
        Info {
            name: "Basic Plugin".to_string(),
            unique_id: 1357, // Used by hosts to differentiate between plugins.

            ..Default::default()
        }
    }
}

plugin_main!(BasicPlugin); // Important!
```
