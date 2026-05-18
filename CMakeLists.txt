cmake_minimum_required(VERSION 3.12)

# Define a project.
project(TEO_GZ_SIM_MODELS LANGUAGES NONE)

# Find dependencies.
find_package(YCM 0.11 REQUIRED)

# Install models and environments.
install(DIRECTORY models worlds
        DESTINATION share/teo-gz-sim-models)

# Store the package in the user registry.
set(CMAKE_EXPORT_PACKAGE_REGISTRY ON)

# Create and install config files.
include(InstallBasicPackageFiles)

install_basic_package_files(${PROJECT_NAME}
                            VERSION 0.1.0
                            COMPATIBILITY AnyNewerVersion
                            NO_EXPORT)

# Add uninstall rule.
include(AddUninstallTarget)
