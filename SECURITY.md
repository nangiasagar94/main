# Security and device-management policy

## Scope

This repository does not attempt to bypass, disable, or interfere with device-management controls, mobile device management (MDM), remote-access protections, or administrator-enforced policies. Those controls must be configured by the authorized device owner or organization administrator through Apple Business Manager, the organization's MDM platform, and approved device-management procedures.

## iOS release requirements

Before publishing an iOS build:

- Keep App Transport Security enabled.
- Use HTTPS for all production API traffic.
- Do not ship debug servers, remote-control endpoints, developer menus, or test credentials in Release builds.
- Store credentials and tokens in the Keychain; never commit them to the repository.
- Review entitlements and provisioning profiles for only the capabilities required by the app.
- Review third-party SDKs and remove unused network, analytics, or remote-management components.
- Validate the App Store version and release notes before distribution.
- Use the organization's authorized administrator process for any MDM or remote-access change.

## App Store updates

An App Store update check can only be implemented after the iOS project, bundle identifier, and App Store ID are available. The check should use Apple's App Store lookup service, handle network failure without blocking the app unexpectedly, and present an optional or mandatory update according to the product's release policy.

No App Store update code is added by this repository change because this repository currently does not contain an iOS project or App Store identifier.
