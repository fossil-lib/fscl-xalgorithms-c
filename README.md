# Fossil XAlgorithms - `C`

XAlgorithms denotes a set of advanced algorithms that go beyond the standard and basic computational routines. These algorithms are often designed to address specific challenges or to optimize performance for particular scenarios. The "x" prefix signifies an extension or augmentation, implying that these algorithms provide enhanced functionalities, improved efficiency, or specialized solutions compared to their more fundamental counterparts. These advanced algorithms may be tailored for specific domains, making them valuable tools in various fields of computer science and software development.

## Prerequisites

Before getting started, make sure you have the following installed:

- **Meson Build System**: This project relies on Meson. If you don't have Meson installed, visit the official [Meson website](https://mesonbuild.com/Getting-meson.html) for installation instructions.

## Setting up, Compiling, Installing, and Running the Project

**Adding Dependency**:

Create a directory named subprojects in the root directory, next create a file named `fscl-xalgorithms-c.wrap` in the `subprojects` directory of your project with the following content:

   ```ini
   [wrap-git]
   url = https://github.com/fossil-lib/fscl-xalgorithms-c.git
   revision = main
   
   [provide]
   fscl-xalgorithms-c = fscl_xalgorithms_c_dep
   ```

**Integrate Dependency**:
   ```meson
   project('my_project', 'c')

   exe = executable('my_project', 'my_project.c',
       dependencies : dependency('fscl-xalgorithms-c')) # add this line

   test('basic', exe)
   ```

## Including the Demo and Running Tests

To run tests, you can use the following options when configuring the build:

- **Running Tests**: Add `-Dwith_test=enabled` when configuring the build.

Example:

```zsh
meson setup builddir -Dwith_test=enabled
```

## Contributing and Support

If you're interested in contributing to this project, encounter any issues, have questions, or would like to provide feedback, don't hesitate to open an issue or visit the [Fossil Logic Docs](https://fossillogic.com/the-docs) for more information.
