# Changelog

All notable changes to this project will be documented in this file.

## [1.4.0] - 2026-04-28

### Collection

- Added *windows11* role to collection.
- Added *windows11_standalone* role to collection.

### Role - rhel8

- Various bug fixes and improvements.

### Role - rhel9

- Various bug fixes and improvements.

### Role - windows2019

- Various bug fixes and improvements.

### Role - windows2022

- Various bug fixes and improvements.

### Role - windows2025

- Various bug fixes and improvements.

## [1.3.3] - 2025-06-10

### Collection

- Corrected missing or extra dependencies.

## [1.3.2] - 2025-06-07

### Collection

- Cleaned up dependencies.
- Changed repository URL to use GitHub Organization.

## [1.3.1] - 2025-06-04

### Role - windows2022

- Fixed missing variable.

## [1.3.0] - 2025-06-04

### Collection

- Added *windows2025* role.

### Role - windows2022

- Updated role to be based on CIS Benchmarks v4.0.0. See the CIS Benchmark document for details.

## [1.2.2] - 2025-03-10

### Role - rhel8

- Fixed include/import tasks paths.

### Role - rhel9

- Fixed include/import tasks paths.

### Role - windows2019

- Fixed include/import tasks paths.

### Role - windows2022

- Fixed include/import tasks paths.

## [1.2.1] - 2025-01-08

### Collection

- Added Changelog.
- Updated collection README documentation.

## [1.2.0] - 2024-11-20

### Role - rhel8

- Updated role to be based on CIS Benchmarks v2.0.0. See the CIS Benchmark document for details.
- Split `rhel8cis_mount_with_uuid` variable into `rhel8cis_home_mount_with_uuid`, `rhel8cis_var_mount_with_uuid`, `rhel8cis_var_log_mount_with_uuid`, `rhel8cis_var_log_audit_mount_with_uuid`, and `rhel8cis_var_tmp_mount_with_uuid` variables to allow UUID mounting to be used on a per mount point basis.

### Role - rhel9

- Updated role to be based on CIS Benchmarks v2.0.0. See the CIS Benchmark document for details.
- Split `rhel9cis_mount_with_uuid` variable into `rhel9cis_home_mount_with_uuid`, `rhel9cis_var_mount_with_uuid`, `rhel9cis_var_log_mount_with_uuid`, `rhel9cis_var_log_audit_mount_with_uuid`, and `rhel9cis_var_tmp_mount_with_uuid` variables to allow UUID mounting to be used on a per mount point basis.

### Role - windows2019

- Updated role to be based on CIS Benchmarks v3.0.1. See the CIS Benchmark document for details.

### Role - windows2022

- Updated role to be based on CIS Benchmarks v3.0.0. See the CIS Benchmark document for details.

## [1.1.1] - 2024-10-22

### Role - windows2019

- Removed `os_family` subset for fact gathering step as it is not used on Windows machines.

### Role - windows2022

- Removed `os_family` subset for fact gathering step as it is not used on Windows machines.

## [1.1.0] - 2024-09-26

### Role - rhel8

- Added `rhel8cis_mount_with_uuid` option (enabled by default) to mount using UUIDs instead of device paths.

### Role - rhel9

- Added `rhel9cis_mount_with_uuid` option (enabled by default) to mount using UUIDs instead of device paths.

## [1.0.9] - 2024-09-10

### Role - rhel9

- Added missing variable `rhel9cis_rule_2_3_2_force`.

## [1.0.8] - 2024-09-06

### Role - rhel8

- Added `rhel8cis_bootloader_password` variable with `no_log` option to allow for setting the bootloader password.

### Role - rhel9

- Added `no_log` option to `rhel9cis_bootloader_password` variable.

## [1.0.7] - 2024-08-09

### Collection

- Minimum Ansible version changed from `2.14` to `2.15` due to EOL status.

## [1.0.6] - 2024-07-08

### Collection

- Updated manifest file to ensure that molecule tests are not included in releases.

## [1.0.5] - 2024-06-30

### Role - windows2019

- Fixed variables that did not match the role argument spec when used in the role.

## [1.0.4] - 2024-06-30

### Role - windows2019

- Renamed `w2022cis_login_message_text` and `w2022cis_login_message_title` variables to `w2019cis_login_message_text` and `w2019cis_login_message_title` variables to match the naming scheme.

## [1.0.3] - 2024-06-30

### Role - windows2019

- Renamed `w2019cis_legal_notice_text` and `w2019cis_legal_notice_title` variables to `w2022cis_login_message_text` and `w2022cis_login_message_title` variables. The name prefixes are fixed in v1.0.4.

### Role - windows2022

- Renamed `w2022cis_legal_notice_text` and `w2022cis_legal_notice_title` variables to `w2022cis_login_message_text` and `w2022cis_login_message_title` variables.

## [1.0.2] - 2024-06-20

### Role - rhel8

- Updated documentation and role metadata for readability.

### Role - rhel9

- Updated documentation and role metadata for readability.

### Role - windows2019

- Updated documentation and role metadata for readability.

### Role - windows2022

- Updated documentation and role metadata for readability.

## [1.0.1] - 2024-06-20

### Role - rhel8

- Removed validation that is handled by role argument spec.

### Role - rhel9

- Removed validation that is handled by role argument spec.

### Role - windows2019

- Removed validation that is handled by role argument spec.

### Role - windows2022

- Removed validation that is handled by role argument spec.

## [1.0.0] - 2024-06-13

### Collection

- Initial release.
- *rhel8* role added.
- *rhel9* role added.
- *windows2019* role added.
- *windows2022* role added.
