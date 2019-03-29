## elsa

[![Build Status](https://travis-ci.com/Manishearth/elsa.svg?branch=master)](https://travis-ci.com/Manishearth/elsa)
[![Current Version](https://meritbadge.herokuapp.com/elsa)](https://crates.io/crates/elsa)
[![License: MIT/Apache-2.0](https://img.shields.io/crates/l/clippy.svg)](#license)

This crate provides various "frozen" collections.

These are append-only collections where references to entries can be held on to even across insertions. This is safe because these collections only support storing data that's present behind some indirection -- i.e. `String`, `Vec<T>`, `Box<T>`, etc, and they only yield references to the data behind the allocation (`&str`, `&[T]`, and `&T` respectively)

The typical use case is having a global cache of strings or other data which the rest of the program borrows from.
