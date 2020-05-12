# Ethos-u

This is the root repository for all Ethos-u software. It is provided to help
users download required repositories and place them in a tree structure.

```
$ ./fetch_externals.py
```

The script will build following tree structure.

```
Directory               Repository
.                       https://review.mlplatform.org/admin/repos/ml/ethos-u/ethos-u
+-- core_software       https://review.mlplatform.org/admin/repos/ml/ethos-u/ethos-u-core-driver
|   +-- core_driver     https://review.mlplatform.org/admin/repos/ml/ethos-u/ethos-u-core-software
|   +-- cmsis           GitHub
|   +-- tensorflow      GitHub
+-- vela                https://review.mlplatform.org/admin/repos/ml/ethos-u/ethos-u-vela
```

| Directory | Description |
--- | ---
| .             | This is the root directory for all Ethos-u software. |
| core_software | The software executing on Arm Cortex-M is referred to as _Core Software_. This folder provides a small build system that illustrates how to build the key components for the Ethos-u core software. |
| cmsis         | CMSIS provides optimized kernels and generic interfaces to the Arm Cortex-M CPUs. |
| tensorflow    | The TensorFlowLite micro framework is used to run inferences. |
| vela          | The Vela optimizer takes a TFLu file as input and replaces operators that are supported by the Ethos-u NPU with custom operators designed to run on the NPU. Operators not supported by the NPU are executed in software. |
