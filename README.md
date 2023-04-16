# cpu_intel_8080_emulator

<p align="center">
      <img src="https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white" alt="rustLogo" style="height:60px;"/>
</p>

## Description

Here is a simple Intel 8080 CPU emulator written in Rust.

I used this processor for my Space Invaders project. You can find it [here](https://github.com/Im-Rises/space_invaders_arcade_emulator).

This emulator passed all the tests of the Intel 8080 CPU. You can find the tests roms in the `test_roms` folder.

## Images

| Title screen                                                                                                           | Game screen                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| ![title_screen](https://user-images.githubusercontent.com/59691442/181736212-8d8cfa4e-4c85-48ce-92ac-1165dcb73891.png) | ![playing_demo](https://user-images.githubusercontent.com/59691442/181736224-da769503-2a2e-45d6-af2c-9204a96e78e1.png) |

| Taito Cop Easter Egg                                                                                                           | Score advance table with Invaders                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| ![taito_cop_easter_egg](https://user-images.githubusercontent.com/59691442/183047666-97f9711c-e2a4-4659-86df-410db5562450.png) | ![score_advance_table](https://user-images.githubusercontent.com/59691442/183058044-b5d532d6-bad2-4629-a55c-f669c82a5e29.png) |

## Videos

https://user-images.githubusercontent.com/59691442/183045566-0a3df947-06e7-4c46-9fc6-9d2b8f7d9a46.mp4

## How to use it

PLACEHOLDER

## Rust tests

You can test the good behaviour of the project by typing the commands onf of the following command. It will start the
unit test of the CPU.

It will start a test rom for the Intel 8080 CPU. You can find it in the link below:  
<https://altairclone.com/downloads/cpu_tests/>

```bash
cargo test
```

<!--
If you want some debug infos about the cpu type:

```bash
cargo test -- --show-output
```
-->

Currently, the CPU is passing the following tests:

- [x] cpudiag.bin
- [x] TST8080.COM
- [x] 8080PRE.COM
- [x] CPUTEST.COM
- [x] 8080EXM.COM

The tests are named:

- cpu_test_rom_cpudiag
- cpu_test_rom_tst8080
- cpu_test_rom_8080pre
- cpu_test_rom_cputest
- cpu_test_rom_8080exm

You can start them individuality by typing:

```bash
cargo test <test_name>
```

or

```bash
cargo test --release
```

Example: If you want to start the cpu_test_rom_tst8080 test.

```bash
cargo test cpu_test_rom_tst8080
```

or

```bash
cargo test cpu_test_rom_tst8080 --release
```

You can also debug the processes by uncommenting the two lines following lines in the `cpu.rs` file in the `test`
module.

~~~
// let mut f = File::create("test_roms/my_output.log").expect("Cannot create debug log file");  
~~~

~~~
// write_debug_to_file(&mut cpu_debug, &mut f, cycles_counter);
~~~

> **Note**  
> Depending on the test the output is different. Refer to this project for more explanation about how they work.  
> https://github.com/superzazu/8080  
> http://www.emulator101.com/full-8080-emulation.html
>
> The last test (cpu_test_rom_8080exm) can take a lot of time in debug mode, you should test it in release mode, use the
> command below:
> ```bash
> cargo test cpu_test_rom_8080exm --release
> ```

## GitHub Actions

[![Rust](https://github.com/Im-Rises/cpu_intel_8080_emulator/actions/workflows/rust.yml/badge.svg?branch=main)](https://github.com/Im-Rises/cpu_intel_8080_emulator/actions/workflows/rust.yml)
[![rust-clippy analyze](https://github.com/Im-Rises/cpu_intel_8080_emulator/actions/workflows/rust-clippy.yml/badge.svg?branch=main)](https://github.com/Im-Rises/cpu_intel_8080_emulator/actions/workflows/rust-clippy.yml)
[![rustfmt check](https://github.com/Im-Rises/cpu_intel_8080_emulator/actions/workflows/rustfmt.yml/badge.svg?branch=main)](https://github.com/Im-Rises/cpu_intel_8080_emulator/actions/workflows/rustfmt.yml)

The project is set with a set of different scripts:

- rust : Check the code compilation.
- rust-clippy analyze : Evaluate the code quality (error, warnings, etc...).
- rustfmt check :  Check the code good formatting

## Documentation

emulator101:  
<http://www.emulator101.com>

Computer Archeology:  
<https://www.computerarcheology.com/Arcade/SpaceInvaders/Hardware.html>

Emudev.de:  
<https://emudev.de/q00-si/a-short-fun-project/>

Rust:  
<https://doc.rust-lang.org/book>

rust-clippy:  
<https://github.com/rust-lang/rust-clippy>

rustfmt:  
<https://github.com/rust-lang/rustfmt>

Intel 8080 documentations:  
<https://archive.org/details/8080Datasheet>  
<https://altairclone.com/downloads/manuals/8080%20Programmers%20Manual.pdf>
<http://bitsavers.org/components/intel/MCS80/9800301D_8080_8085_Assembly_Language_Programming_Manual_May81.pdf>

Intel 8080 opcodes table:  
<https://www.pastraiser.com/cpu/i8080/i8080_opcodes.html>

Wikipedia:  
<https://en.wikipedia.org/wiki/Intel_8080>

Test Roms for the Intel 8080:  
<https://github.com/superzazu/8080/>  
<https://altairclone.com/downloads/cpu_tests/>  
<http://www.emulator101.com/full-8080-emulation.html>

## Contributors

Quentin MOREL :

- @Im-Rises
- <https://github.com/Im-Rises>

[![GitHub contributors](https://contrib.rocks/image?repo=Im-Rises/GameBoyEmulator)](https://github.com/Im-Rises/GameBoyEmulator/graphs/contributors)
