# Minimal build.gradle.kts for compiling protos & generating Kotlin stub code for GRPC
This is a barebones repo showing how to generate Kotlin stub code and compile protos for GRPC from a Gradle buildscript (`build.gradle.kts`).

Here's what you need to do:

1. Put your proto files in `src/main/proto`
2. `gradle generateProto`
3. Look for the generated files in `build/generated/source/proto/main`

## Rationale
The [official gRPC guide to Kotlin](https://www.grpc.io/docs/languages/kotlin/) refers to the collection of [gRPC Kotlin examples](https://github.com/grpc/grpc-kotlin/tree/master/examples) for compiling protos and generating stub code. However, the examples have several projects all together and are therefore kind of complicated. What is the minimal `build.gradle.kts` necessary to automatically generate proto code and stub methods? That is what this repo attempts to provide.

## Notes

- Newer versions of the plugins and dependencies may be available by the time you see this.
- The Gradle buildscript includes just enough to generate the stub code. **You'll need additional dependencies to compile them**; at a minimum, the Kotlin and Protobuf libraries.
