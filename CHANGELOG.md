# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## v0.4.3 (2023-07-18)

### Chore

 - <csr-id-f30a539a69fb8f3f7b18e55c9a3f15ed6642b78d/> update version 0.4 → 0.4.1
 - <csr-id-277c71d6b5c2976e072c815f644908438d810249/> update version 0.3.4 → 0.4
 - <csr-id-dc6ad101841b58da918aa4e236673ab1031adb62/> add rustfmt config

### Documentation

 - <csr-id-4dca3c8b11819f052ac752ce9a31259fef26c041/> version 0.3.2 -> 0.3.3
 - <csr-id-f65ad603b2c40d0214b3881deecb4dd0551c706a/> update version 0.3.1 -> 0.3.2
 - <csr-id-9bfe9f8934aa12fecebad7eea2e64518ff836a69/> update version 0.3.0 -> 0.3.1
 - <csr-id-57a120529967ecae452a19fec303bbdb4dc8e015/> update to version 0.3.0
 - <csr-id-bc30ea3ba4abe9146b5f2b5b174d5d5b8a898226/> update version to 0.2.0
 - <csr-id-69497d3c55f950b37d579d5a73830d9ef96af97d/> fix dependency name
 - <csr-id-8100e577f179327b1aee3d4bab8aa28feec620a1/> remove duplicate fields
 - <csr-id-34c48e492be4e0f599b2511138bbefa0a84f8960/> add info to cargo.toml

### New Features

 - <csr-id-0e49aa6755a915ff19689c5df7d9a5a2b43eb8e9/> add 'as_ptr' method
 - <csr-id-2722a24a81bf58bdde7aedb402c2e381e67a9680/> add non thread-safe owned pool
 - <csr-id-d00ff2cafe7caad557df360f5bbab2a3971488d2/> remove 'allocate' mutable requirement
   Since both variants of the pool has interior mutability, it is not worth
   the cost of an additional wrapper (`Mutex` or `RefCell`) for the
   semantic purpose of a mutable `allocate` method.
 - <csr-id-bd41826b7de2520e1bac4a63e7a027a5bc71733e/> add allocations method
 - <csr-id-338c1261b94a926fc37b2dfdcea2feb66c5ab1d5/> make SlicePool thread-safe
 - <csr-id-286d1cd8253fd08b83982684f790057e5d763049/> add 'as_ptr' functionmethod
 - <csr-id-1b0dccfd923eae9858e5b445e6e32b99c4d5408a/> add owned slice pool
 - <csr-id-953420dde89d80675c7f2c5e3f5bbc627f7e5c8d/> initial commit

### Bug Fixes

 - <csr-id-0a0bddc074629b8e850c985647e1434a0cdab32d/> make pool depend on template type for `Send`

### Refactor

 - <csr-id-31d286c84cacc3ee2092e3921c2db008d0bc00e5/> complete rewrite of 'SlicePool'
   The previous implementation suffered from memory unsafety and poor
   performance. This new design should improve the performance as well as
   ensuring memory and thread safety. The abstractions have also improved
   and the code is much more readable.
   
   Currently the 'unsync' variants and reference 'SlicePool' is not
   implemented.
 - <csr-id-541012af959cfe07797eb34d833e6535f7e6ac2f/> rename SlicePool -> SlicePoolRef
 - <csr-id-a4c6b0eee52cdd50dc188650f4810a5f32f5d304/> make len return size instead

### Commit Statistics

<csr-read-only-do-not-edit/>

 - 33 commits contributed to the release over the course of 2413 calendar days.
 - 23 commits were understood as [conventional](https://www.conventionalcommits.org).
 - 0 issues like '(#ID)' were seen in commit messages

### Commit Details

<csr-read-only-do-not-edit/>

<details><summary>view details</summary>

 * **Uncategorized**
    - Merge pull request #1 from Hpmason/fix-warnings ([`714f496`](https://github.com/Hpmason/slice-pool-rs/commit/714f496fe7c10fe290daefc4b10984657b66612b))
    - Fix clippy warnings ([`0f896dc`](https://github.com/Hpmason/slice-pool-rs/commit/0f896dc0745219b9314d10c2d536e79c1f646f39))
    - Update edition to 2021 ([`b2ea621`](https://github.com/Hpmason/slice-pool-rs/commit/b2ea621ccab79d7ca5d5e78ec685c70e9d10b3cd))
    - Fix doc link ([`0fc1182`](https://github.com/Hpmason/slice-pool-rs/commit/0fc1182c72d279b7decfb0f56568f8e0434a3fe4))
    - Add changelog ([`aa80dc6`](https://github.com/Hpmason/slice-pool-rs/commit/aa80dc631af9b6043c94057919a7bcf5b4d56d46))
    - Release slice-pool2 v0.4.2 ([`0a8b385`](https://github.com/Hpmason/slice-pool-rs/commit/0a8b385135e3349c1be0146c508439f7b82aac72))
    - Update crate info for publishing ([`b7d2a87`](https://github.com/Hpmason/slice-pool-rs/commit/b7d2a871d23629fea504abbc71dbbc4a478e2850))
    - Simplify merge operation. ([`12460e7`](https://github.com/Hpmason/slice-pool-rs/commit/12460e7f69ad8bd74fdcdf67f9923a68bbf8ec9e))
    - Fix bug in complex fragmentation situation. ([`0de5ba6`](https://github.com/Hpmason/slice-pool-rs/commit/0de5ba6dce73f6d5f5390849fdccd4ce29a5e579))
    - Update version 0.4 → 0.4.1 ([`f30a539`](https://github.com/Hpmason/slice-pool-rs/commit/f30a539a69fb8f3f7b18e55c9a3f15ed6642b78d))
    - Add 'as_ptr' method ([`0e49aa6`](https://github.com/Hpmason/slice-pool-rs/commit/0e49aa6755a915ff19689c5df7d9a5a2b43eb8e9))
    - Update version 0.3.4 → 0.4 ([`277c71d`](https://github.com/Hpmason/slice-pool-rs/commit/277c71d6b5c2976e072c815f644908438d810249))
    - Add non thread-safe owned pool ([`2722a24`](https://github.com/Hpmason/slice-pool-rs/commit/2722a24a81bf58bdde7aedb402c2e381e67a9680))
    - Add rustfmt config ([`dc6ad10`](https://github.com/Hpmason/slice-pool-rs/commit/dc6ad101841b58da918aa4e236673ab1031adb62))
    - Complete rewrite of 'SlicePool' ([`31d286c`](https://github.com/Hpmason/slice-pool-rs/commit/31d286c84cacc3ee2092e3921c2db008d0bc00e5))
    - (cargo-release) version 0.3.4 ([`e910def`](https://github.com/Hpmason/slice-pool-rs/commit/e910defc0791f636dbfe700c34624e65666143c9))
    - Make pool depend on template type for `Send` ([`0a0bddc`](https://github.com/Hpmason/slice-pool-rs/commit/0a0bddc074629b8e850c985647e1434a0cdab32d))
    - Remove 'allocate' mutable requirement ([`d00ff2c`](https://github.com/Hpmason/slice-pool-rs/commit/d00ff2cafe7caad557df360f5bbab2a3971488d2))
    - Version 0.3.2 -> 0.3.3 ([`4dca3c8`](https://github.com/Hpmason/slice-pool-rs/commit/4dca3c8b11819f052ac752ce9a31259fef26c041))
    - Add allocations method ([`bd41826`](https://github.com/Hpmason/slice-pool-rs/commit/bd41826b7de2520e1bac4a63e7a027a5bc71733e))
    - Update version 0.3.1 -> 0.3.2 ([`f65ad60`](https://github.com/Hpmason/slice-pool-rs/commit/f65ad603b2c40d0214b3881deecb4dd0551c706a))
    - Make SlicePool thread-safe ([`338c126`](https://github.com/Hpmason/slice-pool-rs/commit/338c1261b94a926fc37b2dfdcea2feb66c5ab1d5))
    - Update version 0.3.0 -> 0.3.1 ([`9bfe9f8`](https://github.com/Hpmason/slice-pool-rs/commit/9bfe9f8934aa12fecebad7eea2e64518ff836a69))
    - Add 'as_ptr' functionmethod ([`286d1cd`](https://github.com/Hpmason/slice-pool-rs/commit/286d1cd8253fd08b83982684f790057e5d763049))
    - Update to version 0.3.0 ([`57a1205`](https://github.com/Hpmason/slice-pool-rs/commit/57a120529967ecae452a19fec303bbdb4dc8e015))
    - Add owned slice pool ([`1b0dccf`](https://github.com/Hpmason/slice-pool-rs/commit/1b0dccfd923eae9858e5b445e6e32b99c4d5408a))
    - Update version to 0.2.0 ([`bc30ea3`](https://github.com/Hpmason/slice-pool-rs/commit/bc30ea3ba4abe9146b5f2b5b174d5d5b8a898226))
    - Rename SlicePool -> SlicePoolRef ([`541012a`](https://github.com/Hpmason/slice-pool-rs/commit/541012af959cfe07797eb34d833e6535f7e6ac2f))
    - Make len return size instead ([`a4c6b0e`](https://github.com/Hpmason/slice-pool-rs/commit/a4c6b0eee52cdd50dc188650f4810a5f32f5d304))
    - Fix dependency name ([`69497d3`](https://github.com/Hpmason/slice-pool-rs/commit/69497d3c55f950b37d579d5a73830d9ef96af97d))
    - Remove duplicate fields ([`8100e57`](https://github.com/Hpmason/slice-pool-rs/commit/8100e577f179327b1aee3d4bab8aa28feec620a1))
    - Add info to cargo.toml ([`34c48e4`](https://github.com/Hpmason/slice-pool-rs/commit/34c48e492be4e0f599b2511138bbefa0a84f8960))
    - Initial commit ([`953420d`](https://github.com/Hpmason/slice-pool-rs/commit/953420dde89d80675c7f2c5e3f5bbc627f7e5c8d))
</details>

## v0.4.2 (2023-07-16)

<csr-id-f30a539a69fb8f3f7b18e55c9a3f15ed6642b78d/>
<csr-id-277c71d6b5c2976e072c815f644908438d810249/>
<csr-id-dc6ad101841b58da918aa4e236673ab1031adb62/>
<csr-id-31d286c84cacc3ee2092e3921c2db008d0bc00e5/>
<csr-id-541012af959cfe07797eb34d833e6535f7e6ac2f/>
<csr-id-a4c6b0eee52cdd50dc188650f4810a5f32f5d304/>

### Chore

 - <csr-id-f30a539a69fb8f3f7b18e55c9a3f15ed6642b78d/> update version 0.4 → 0.4.1
 - <csr-id-277c71d6b5c2976e072c815f644908438d810249/> update version 0.3.4 → 0.4
 - <csr-id-dc6ad101841b58da918aa4e236673ab1031adb62/> add rustfmt config

### Documentation

 - <csr-id-4dca3c8b11819f052ac752ce9a31259fef26c041/> version 0.3.2 -> 0.3.3
 - <csr-id-f65ad603b2c40d0214b3881deecb4dd0551c706a/> update version 0.3.1 -> 0.3.2
 - <csr-id-9bfe9f8934aa12fecebad7eea2e64518ff836a69/> update version 0.3.0 -> 0.3.1
 - <csr-id-57a120529967ecae452a19fec303bbdb4dc8e015/> update to version 0.3.0
 - <csr-id-bc30ea3ba4abe9146b5f2b5b174d5d5b8a898226/> update version to 0.2.0
 - <csr-id-69497d3c55f950b37d579d5a73830d9ef96af97d/> fix dependency name
 - <csr-id-8100e577f179327b1aee3d4bab8aa28feec620a1/> remove duplicate fields
 - <csr-id-34c48e492be4e0f599b2511138bbefa0a84f8960/> add info to cargo.toml

### New Features

 - <csr-id-0e49aa6755a915ff19689c5df7d9a5a2b43eb8e9/> add 'as_ptr' method
 - <csr-id-2722a24a81bf58bdde7aedb402c2e381e67a9680/> add non thread-safe owned pool
 - <csr-id-d00ff2cafe7caad557df360f5bbab2a3971488d2/> remove 'allocate' mutable requirement
   Since both variants of the pool has interior mutability, it is not worth
   the cost of an additional wrapper (`Mutex` or `RefCell`) for the
   semantic purpose of a mutable `allocate` method.
 - <csr-id-bd41826b7de2520e1bac4a63e7a027a5bc71733e/> add allocations method
 - <csr-id-338c1261b94a926fc37b2dfdcea2feb66c5ab1d5/> make SlicePool thread-safe
 - <csr-id-286d1cd8253fd08b83982684f790057e5d763049/> add 'as_ptr' functionmethod
 - <csr-id-1b0dccfd923eae9858e5b445e6e32b99c4d5408a/> add owned slice pool
 - <csr-id-953420dde89d80675c7f2c5e3f5bbc627f7e5c8d/> initial commit

### Bug Fixes

 - <csr-id-0a0bddc074629b8e850c985647e1434a0cdab32d/> make pool depend on template type for `Send`

### Refactor

 - <csr-id-31d286c84cacc3ee2092e3921c2db008d0bc00e5/> complete rewrite of 'SlicePool'
   The previous implementation suffered from memory unsafety and poor
   performance. This new design should improve the performance as well as
   ensuring memory and thread safety. The abstractions have also improved
   and the code is much more readable.
   
   Currently the 'unsync' variants and reference 'SlicePool' is not
   implemented.
 - <csr-id-541012af959cfe07797eb34d833e6535f7e6ac2f/> rename SlicePool -> SlicePoolRef
 - <csr-id-a4c6b0eee52cdd50dc188650f4810a5f32f5d304/> make len return size instead

