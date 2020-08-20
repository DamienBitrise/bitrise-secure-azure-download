# bitrise-secure-azure-download
Simple Ruby based secure Azure Download

## Required Secrets
- AZURE_ACCOUNT_NAME
- AZURE_ACCOUNT_KEY
- AZURE_CONTAINER

**bitrise.yml snippet:**

- git::https://github.com/DamienBitrise/bitrise-secure-azure-download@master:
        inputs:
        - account_name: "$AZURE_ACCOUNT_NAME"
        - account_key: "$AZURE_ACCOUNT_KEY"
        - container: "$AZURE_CONTAINER"
        - object: "$BITRISE_BUILD_SLUG.zip"
        - filename: "$BITRISE_SOURCE_DIR/DerivedData_downloaded.zip"
