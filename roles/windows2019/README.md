<!-- BEGIN_ANSIBLE_DOCS -->

# Ansible Role: trippsc2.cis.windows2019
Version: 1.3.3

This role applies the CIS Benchmark hardening steps on Windows Server 2019 machines. It is based on the CIS Benchmark for Windows Server 2019, v3.0.1.


## Requirements

| Platform | Versions |
| -------- | -------- |
| Windows | <ul><li>2019</li></ul> |

## Dependencies

| Collection |
| ---------- |
| ansible.windows |
| community.windows |

## Role Arguments
|Option|Description|Type|Required|Choices|Default|
|---|---|---|---|---|---|
| w2019cis_skip_reboot | <p>Whether to skip rebooting the machine.</p> | bool | no |  | False |
| w2019cis_level | <p>The CIS Benchmark level to apply.</p><p>Level 3 refers to Next Generation Windows Security (NGWS) benchmarks.</p> | int | no | <ul><li>1</li><li>2</li><li>3</li></ul> | 3 |
| w2019cis_is_template | <p>Whether to apply the CIS Benchmark as a template.</p><p>If true, only apply the benchmarks that apply to standalone, domain members, and domain controllers are applied.</p> | bool | no |  | False |
| w2019cis_rule_1_1_1_enabled | <p>Whether to enable rule 1.1.1.</p> | bool | no |  | True |
| w2019cis_rule_1_1_2_enabled | <p>Whether to enable rule 1.1.2.</p> | bool | no |  | True |
| w2019cis_rule_1_1_3_enabled | <p>Whether to enable rule 1.1.3.</p> | bool | no |  | True |
| w2019cis_rule_1_1_4_enabled | <p>Whether to enable rule 1.1.4.</p> | bool | no |  | True |
| w2019cis_rule_1_1_5_enabled | <p>Whether to enable rule 1.1.5.</p> | bool | no |  | True |
| w2019cis_rule_1_1_6_enabled | <p>Whether to enable rule 1.1.6.</p> | bool | no |  | True |
| w2019cis_password_history_size | <p>The number of passwords to remember.</p> | int | no |  | 24 |
| w2019cis_maximum_password_age | <p>The maximum password age in days.</p> | int | no |  | 365 |
| w2019cis_minimum_password_age | <p>The minimum password age in days.</p> | int | no |  | 1 |
| w2019cis_minimum_password_length | <p>The minimum password length.</p> | int | no |  | 14 |
| w2019cis_rule_1_2_1_enabled | <p>Whether to enable rule 1.2.1.</p> | bool | no |  | True |
| w2019cis_rule_1_2_2_enabled | <p>Whether to enable rule 1.2.2.</p> | bool | no |  | True |
| w2019cis_rule_1_2_3_enabled | <p>Whether to enable rule 1.2.3.</p> | bool | no |  | True |
| w2019cis_rule_1_2_4_enabled | <p>Whether to enable rule 1.2.4.</p> | bool | no |  | True |
| w2019cis_lockout_duration_in_minutes | <p>The lockout duration in minutes.</p> | int | no |  | 15 |
| w2019cis_lockout_bad_logon_count | <p>The number of bad logon attempts before lockout.</p> | int | no |  | 5 |
| w2019cis_lockout_reset_time_in_minutes | <p>The lockout reset time in minutes.</p> | int | no |  | 15 |
| w2019cis_rule_2_2_1_enabled | <p>Whether to enable rule 2.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_2_enabled | <p>Whether to enable rule 2.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_3_enabled | <p>Whether to enable rule 2.2.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_4_enabled | <p>Whether to enable rule 2.2.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_5_enabled | <p>Whether to enable rule 2.2.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_6_enabled | <p>Whether to enable rule 2.2.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_7_enabled | <p>Whether to enable rule 2.2.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_8_enabled | <p>Whether to enable rule 2.2.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_9_enabled | <p>Whether to enable rule 2.2.9.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_10_enabled | <p>Whether to enable rule 2.2.10.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_11_enabled | <p>Whether to enable rule 2.2.11.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_12_enabled | <p>Whether to enable rule 2.2.12.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_13_enabled | <p>Whether to enable rule 2.2.13.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_14_enabled | <p>Whether to enable rule 2.2.14.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_15_enabled | <p>Whether to enable rule 2.2.15.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_16_enabled | <p>Whether to enable rule 2.2.16.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_17_enabled | <p>Whether to enable rule 2.2.17.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_18_enabled | <p>Whether to enable rule 2.2.18.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_19_enabled | <p>Whether to enable rule 2.2.19.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_20_enabled | <p>Whether to enable rule 2.2.20.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_21_enabled | <p>Whether to enable rule 2.2.21.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_22_enabled | <p>Whether to enable rule 2.2.22.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_23_enabled | <p>Whether to enable rule 2.2.23.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_24_enabled | <p>Whether to enable rule 2.2.24.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_25_enabled | <p>Whether to enable rule 2.2.25.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_26_enabled | <p>Whether to enable rule 2.2.26.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_27_enabled | <p>Whether to enable rule 2.2.27.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_28_enabled | <p>Whether to enable rule 2.2.28.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_29_enabled | <p>Whether to enable rule 2.2.29.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_30_enabled | <p>Whether to enable rule 2.2.30.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_31_enabled | <p>Whether to enable rule 2.2.31.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_32_enabled | <p>Whether to enable rule 2.2.32.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_33_enabled | <p>Whether to enable rule 2.2.33.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_34_enabled | <p>Whether to enable rule 2.2.34.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_35_enabled | <p>Whether to enable rule 2.2.35.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_36_enabled | <p>Whether to enable rule 2.2.36.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_37_enabled | <p>Whether to enable rule 2.2.37.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_37_force | <p>Whether to override the level requirement for CIS rule 2.2.37.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_2_2_38_enabled | <p>Whether to enable rule 2.2.38.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_39_enabled | <p>Whether to enable rule 2.2.39.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_40_enabled | <p>Whether to enable rule 2.2.40.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_41_enabled | <p>Whether to enable rule 2.2.41.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_42_enabled | <p>Whether to enable rule 2.2.42.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_43_enabled | <p>Whether to enable rule 2.2.43.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_44_enabled | <p>Whether to enable rule 2.2.44.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_45_enabled | <p>Whether to enable rule 2.2.45.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_46_enabled | <p>Whether to enable rule 2.2.46.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_47_enabled | <p>Whether to enable rule 2.2.47.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_48_enabled | <p>Whether to enable rule 2.2.48.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_2_49_enabled | <p>Whether to enable rule 2.2.49.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_access_this_computer_from_the_network_additional_users | <p>Additional users to grant `Access this computer from the network` permissions.</p> | list of 'str' | no |  | [] |
| w2019cis_adjust_memory_quotas_for_a_process_additional_users | <p>Additional users to grant `Adjust memory quotas for a process` permissions.</p> | list of 'str' | no |  | [] |
| w2019cis_create_global_objects_additional_users | <p>Additional users to grant `Create global objects` permissions.</p> | list of 'str' | no |  | [] |
| w2019cis_debug_programs_additional_users | <p>Additional users to grant `Debug programs` permissions.</p> | list of 'str' | no |  | [] |
| w2019cis_generate_security_audits_additional_users | <p>Additional users to grant `Generate security audits` permissions.</p> | list of 'str' | no |  | [] |
| w2019cis_impersonate_a_client_after_authentication_additional_users | <p>Additional users to grant `Impersonate a client after authentication` permissions.</p> | list of 'str' | no |  | [] |
| w2019cis_manage_auditing_and_security_log_additional_users | <p>Additional users to grant `Manage auditing and security log` permissions.</p> | list of 'str' | no |  | [] |
| w2019cis_perform_volume_maintenance_tasks_additional_users | <p>Additional users to grant `Perform volume maintenance tasks` permissions.</p> | list of 'str' | no |  | [] |
| w2019cis_replace_a_process_level_token_additional_users | <p>Additional users to grant `Replace a process level token` permissions.</p> | list of 'str' | no |  | [] |
| w2019cis_rule_2_3_1_1_enabled | <p>Whether to enable rule 2.3.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_1_2_enabled | <p>Whether to enable rule 2.3.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_1_3_enabled | <p>Whether to enable rule 2.3.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_1_4_enabled | <p>Whether to enable rule 2.3.1.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_admin_username | <p>The name to which to set the default Administrator account.</p> | str | no |  |  |
| w2019cis_guest_username | <p>The name to which to set the default Guest account.</p> | str | no |  |  |
| w2019cis_rule_2_3_2_1_enabled | <p>Whether to enable rule 2.3.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_2_2_enabled | <p>Whether to enable rule 2.3.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_4_1_enabled | <p>Whether to enable rule 2.3.4.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_5_1_enabled | <p>Whether to enable rule 2.3.5.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_5_2_enabled | <p>Whether to enable rule 2.3.5.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_5_3_enabled | <p>Whether to enable rule 2.3.5.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_5_4_enabled | <p>Whether to enable rule 2.3.5.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_5_5_enabled | <p>Whether to enable rule 2.3.5.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_6_1_enabled | <p>Whether to enable rule 2.3.6.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_6_2_enabled | <p>Whether to enable rule 2.3.6.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_6_3_enabled | <p>Whether to enable rule 2.3.6.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_6_4_enabled | <p>Whether to enable rule 2.3.6.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_6_5_enabled | <p>Whether to enable rule 2.3.6.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_6_6_enabled | <p>Whether to enable rule 2.3.6.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_maximum_machine_account_password_age_in_days | <p>The maximum machine account password age in days.</p> | int | no |  | 30 |
| w2019cis_rule_2_3_7_1_enabled | <p>Whether to enable rule 2.3.7.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_7_2_enabled | <p>Whether to enable rule 2.3.7.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_7_3_enabled | <p>Whether to enable rule 2.3.7.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_7_4_enabled | <p>Whether to enable rule 2.3.7.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_7_5_enabled | <p>Whether to enable rule 2.3.7.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_7_6_enabled | <p>Whether to enable rule 2.3.7.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_7_6_force | <p>Whether to override the level requirement for CIS rule 2.3.7.6.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_2_3_7_7_enabled | <p>Whether to enable rule 2.3.7.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_7_8_enabled | <p>Whether to enable rule 2.3.7.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_7_9_enabled | <p>Whether to enable rule 2.3.7.9.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_inactivity_timeout_in_seconds | <p>The inactivity timeout in seconds.</p> | int | no |  | 900 |
| w2019cis_login_message_text | <p>The legal notice text.</p> | str | no |  |  |
| w2019cis_login_message_title | <p>The legal notice caption.</p> | str | no |  |  |
| w2019cis_cached_logons_count | <p>The number of cached logons to remember.</p> | int | no |  | 4 |
| w2019cis_password_expiry_warning_in_days | <p>The password expiry warning in days.</p> | int | no |  | 14 |
| w2019cis_smart_card_removal_behavior | <p>The smart card removal behavior.</p> | str | no | <ul><li>lock</li><li>logoff</li><li>disconnect</li></ul> | lock |
| w2019cis_rule_2_3_8_1_enabled | <p>Whether to enable rule 2.3.8.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_8_2_enabled | <p>Whether to enable rule 2.3.8.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_8_3_enabled | <p>Whether to enable rule 2.3.8.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_9_1_enabled | <p>Whether to enable rule 2.3.9.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_9_2_enabled | <p>Whether to enable rule 2.3.9.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_9_3_enabled | <p>Whether to enable rule 2.3.9.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_9_4_enabled | <p>Whether to enable rule 2.3.9.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_9_5_enabled | <p>Whether to enable rule 2.3.9.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019_idle_smb_timeout_in_minutes | <p>The idle SMB timeout in minutes.</p> | int | no |  | 15 |
| w2019cis_smb_spn_target_name_validation_level | <p>The SMB SPN target name validation level.</p> | str | no | <ul><li>accept</li><li>required</li></ul> | required |
| w2019cis_rule_2_3_10_1_enabled | <p>Whether to enable rule 2.3.10.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_10_2_enabled | <p>Whether to enable rule 2.3.10.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_10_3_enabled | <p>Whether to enable rule 2.3.10.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_10_4_enabled | <p>Whether to enable rule 2.3.10.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_10_4_force | <p>Whether to override the level requirement for CIS rule 2.3.10.4.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_2_3_10_5_enabled | <p>Whether to enable rule 2.3.10.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_10_6_enabled | <p>Whether to enable rule 2.3.10.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_10_7_enabled | <p>Whether to enable rule 2.3.10.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_10_8_enabled | <p>Whether to enable rule 2.3.10.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_10_9_enabled | <p>Whether to enable rule 2.3.10.9.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_10_10_enabled | <p>Whether to enable rule 2.3.10.10.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_10_11_enabled | <p>Whether to enable rule 2.3.10.11.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_10_12_enabled | <p>Whether to enable rule 2.3.10.12.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_10_13_enabled | <p>Whether to enable rule 2.3.10.13.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_null_session_pipes | <p>The null session pipes.</p> | list of 'str' | no |  | [] |
| w2019cis_remote_registry_paths | <p>The remote registry paths.</p> | list of 'str' | no |  | ['System\\CurrentControlSet\\Control\\Print\\Printers', 'System\\CurrentControlSet\\Services\\Eventlog', 'Software\\Microsoft\\OLAP Server', 'Software\\Microsoft\\Windows NT\\CurrentVersion\\Print', 'Software\\Microsoft\\Windows NT\\CurrentVersion\\Windows', 'System\\CurrentControlSet\\Control\\ContentIndex', 'System\\CurrentControlSet\\Control\\Terminal Server', 'System\\CurrentControlSet\\Control\\Terminal Server\\UserConfig', 'System\\CurrentControlSet\\Control\\Terminal Server\\DefaultUserConfiguration', 'Software\\Microsoft\\Windows NT\\CurrentVersion\\Perflib', 'System\\CurrentControlSet\\Services\\SysmonLog'] |
| w2019cis_rule_2_3_11_1_enabled | <p>Whether to enable rule 2.3.11.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_11_2_enabled | <p>Whether to enable rule 2.3.11.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_11_3_enabled | <p>Whether to enable rule 2.3.11.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_11_4_enabled | <p>Whether to enable rule 2.3.11.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_11_5_enabled | <p>Whether to enable rule 2.3.11.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_11_6_enabled | <p>Whether to enable rule 2.3.11.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_11_7_enabled | <p>Whether to enable rule 2.3.11.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_11_8_enabled | <p>Whether to enable rule 2.3.11.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_11_9_enabled | <p>Whether to enable rule 2.3.11.9.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_11_10_enabled | <p>Whether to enable rule 2.3.11.10.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_11_11_enabled | <p>Whether to enable rule 2.3.11.11.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_11_12_enabled | <p>Whether to enable rule 2.3.11.12.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_11_13_enabled | <p>Whether to enable rule 2.3.11.13.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_ldap_client_signing_requirements | <p>The LDAP client signing requirements.</p> | str | no | <ul><li>require</li><li>negotiate</li></ul> | require |
| w2019cis_outgoing_ntlm_traffic_requirement | <p>The outgoing NTLM traffic requirement.</p> | str | no | <ul><li>audit_all</li><li>deny_all</li></ul> | audit_all |
| w2019cis_rule_2_3_13_1_enabled | <p>Whether to enable rule 2.3.13.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_15_1_enabled | <p>Whether to enable rule 2.3.15.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_15_2_enabled | <p>Whether to enable rule 2.3.15.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_17_1_enabled | <p>Whether to enable rule 2.3.17.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_17_2_enabled | <p>Whether to enable rule 2.3.17.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_17_3_enabled | <p>Whether to enable rule 2.3.17.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_17_4_enabled | <p>Whether to enable rule 2.3.17.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_17_5_enabled | <p>Whether to enable rule 2.3.17.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_17_6_enabled | <p>Whether to enable rule 2.3.17.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_17_7_enabled | <p>Whether to enable rule 2.3.17.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_2_3_17_8_enabled | <p>Whether to enable rule 2.3.17.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_admin_uac_elevation_behavior | <p>The UAC elevation behavior for administrators.</p> | str | no | <ul><li>prompt_for_credentials</li><li>prompt_for_consent</li></ul> | prompt_for_consent |
| w2019cis_rule_5_1_enabled | <p>Whether to enable rule 5.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_5_2_enabled | <p>Whether to enable rule 5.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_5_2_force | <p>Whether to override the level requirement for CIS rule 5.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_9_1_1_enabled | <p>Whether to enable rule 9.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_9_1_2_enabled | <p>Whether to enable rule 9.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_9_1_3_enabled | <p>Whether to enable rule 9.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_9_1_4_enabled | <p>Whether to enable rule 9.1.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_9_1_5_enabled | <p>Whether to enable rule 9.1.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_9_1_6_enabled | <p>Whether to enable rule 9.1.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_9_1_7_enabled | <p>Whether to enable rule 9.1.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_domain_firewall_log_path | <p>The path to the domain firewall log.</p> | str | no |  | %SystemRoot%\System32\logfiles\firewall\domainfw.log |
| w2019cis_domain_firewall_log_size_in_kb | <p>The size of the domain firewall log in KB.</p> | int | no |  | 16384 |
| w2019cis_rule_9_2_1_enabled | <p>Whether to enable rule 9.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_9_2_2_enabled | <p>Whether to enable rule 9.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_9_2_3_enabled | <p>Whether to enable rule 9.2.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_9_2_4_enabled | <p>Whether to enable rule 9.2.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_9_2_5_enabled | <p>Whether to enable rule 9.2.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_9_2_6_enabled | <p>Whether to enable rule 9.2.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_9_2_7_enabled | <p>Whether to enable rule 9.2.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_private_firewall_log_path | <p>The path to the private firewall log.</p> | str | no |  | %SystemRoot%\System32\logfiles\firewall\privatefw.log |
| w2019cis_private_firewall_log_size_in_kb | <p>The size of the private firewall log in KB.</p> | int | no |  | 16384 |
| w2019cis_rule_9_3_1_enabled | <p>Whether to enable rule 9.3.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_9_3_2_enabled | <p>Whether to enable rule 9.3.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_9_3_3_enabled | <p>Whether to enable rule 9.3.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_9_3_4_enabled | <p>Whether to enable rule 9.3.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_9_3_5_enabled | <p>Whether to enable rule 9.3.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_9_3_6_enabled | <p>Whether to enable rule 9.3.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_9_3_7_enabled | <p>Whether to enable rule 9.3.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_9_3_8_enabled | <p>Whether to enable rule 9.3.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_9_3_9_enabled | <p>Whether to enable rule 9.3.9.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_public_firewall_log_path | <p>The path to the public firewall log.</p> | str | no |  | %SystemRoot%\System32\logfiles\firewall\publicfw.log |
| w2019cis_public_firewall_log_size_in_kb | <p>The size of the public firewall log in KB.</p> | int | no |  | 16384 |
| w2019cis_rule_17_1_1_enabled | <p>Whether to enable rule 17.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_1_2_enabled | <p>Whether to enable rule 17.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_1_3_enabled | <p>Whether to enable rule 17.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_2_1_enabled | <p>Whether to enable rule 17.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_2_2_enabled | <p>Whether to enable rule 17.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_2_3_enabled | <p>Whether to enable rule 17.2.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_2_4_enabled | <p>Whether to enable rule 17.2.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_2_5_enabled | <p>Whether to enable rule 17.2.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_2_6_enabled | <p>Whether to enable rule 17.2.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_3_1_enabled | <p>Whether to enable rule 17.3.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_3_2_enabled | <p>Whether to enable rule 17.3.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_4_1_enabled | <p>Whether to enable rule 17.4.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_4_2_enabled | <p>Whether to enable rule 17.4.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_5_1_enabled | <p>Whether to enable rule 17.5.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_5_2_enabled | <p>Whether to enable rule 17.5.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_5_3_enabled | <p>Whether to enable rule 17.5.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_5_4_enabled | <p>Whether to enable rule 17.5.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_5_5_enabled | <p>Whether to enable rule 17.5.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_5_6_enabled | <p>Whether to enable rule 17.5.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_6_1_enabled | <p>Whether to enable rule 17.6.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_6_2_enabled | <p>Whether to enable rule 17.6.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_6_3_enabled | <p>Whether to enable rule 17.6.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_6_4_enabled | <p>Whether to enable rule 17.6.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_7_1_enabled | <p>Whether to enable rule 17.7.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_7_2_enabled | <p>Whether to enable rule 17.7.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_7_3_enabled | <p>Whether to enable rule 17.7.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_7_4_enabled | <p>Whether to enable rule 17.7.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_7_5_enabled | <p>Whether to enable rule 17.7.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_8_1_enabled | <p>Whether to enable rule 17.8.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_9_1_enabled | <p>Whether to enable rule 17.9.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_9_2_enabled | <p>Whether to enable rule 17.9.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_9_3_enabled | <p>Whether to enable rule 17.9.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_9_4_enabled | <p>Whether to enable rule 17.9.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_17_9_5_enabled | <p>Whether to enable rule 17.9.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_1_1_1_enabled | <p>Whether to enable rule 18.1.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_1_1_2_enabled | <p>Whether to enable rule 18.1.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_1_2_2_enabled | <p>Whether to enable rule 18.1.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_1_3_enabled | <p>Whether to enable rule 18.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_1_3_force | <p>Whether to override the level requirement for CIS rule 18.1.3.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_4_1_enabled | <p>Whether to enable rule 18.4.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_4_2_enabled | <p>Whether to enable rule 18.4.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_4_3_enabled | <p>Whether to enable rule 18.4.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_4_4_enabled | <p>Whether to enable rule 18.4.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_4_5_enabled | <p>Whether to enable rule 18.4.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_4_6_enabled | <p>Whether to enable rule 18.4.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_4_7_enabled | <p>Whether to enable rule 18.4.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_4_8_enabled | <p>Whether to enable rule 18.4.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_5_1_enabled | <p>Whether to enable rule 18.5.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_5_2_enabled | <p>Whether to enable rule 18.5.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_5_3_enabled | <p>Whether to enable rule 18.5.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_5_4_enabled | <p>Whether to enable rule 18.5.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_5_5_enabled | <p>Whether to enable rule 18.5.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_5_5_force | <p>Whether to override the level requirement for CIS rule 18.5.5.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_5_6_enabled | <p>Whether to enable rule 18.5.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_5_7_enabled | <p>Whether to enable rule 18.5.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_5_7_force | <p>Whether to override the level requirement for CIS rule 18.5.7.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_5_8_enabled | <p>Whether to enable rule 18.5.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_5_9_enabled | <p>Whether to enable rule 18.5.9.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_5_10_enabled | <p>Whether to enable rule 18.5.10.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_5_10_force | <p>Whether to override the level requirement for CIS rule 18.5.10.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_5_11_enabled | <p>Whether to enable rule 18.5.11.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_5_11_force | <p>Whether to override the level requirement for CIS rule 18.5.11.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_5_12_enabled | <p>Whether to enable rule 18.5.12.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_screensaver_grace_period_in_seconds | <p>The screensaver grace period in seconds.</p> | int | no |  | 5 |
| w2019cis_security_log_warning_level | <p>The percentage of the security log that must be filled before a warning event is generated.</p> | int | no |  | 90 |
| w2019cis_rule_18_6_4_1_enabled | <p>Whether to enable rule 18.6.4.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_6_4_2_enabled | <p>Whether to enable rule 18.6.4.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_6_4_3_enabled | <p>Whether to enable rule 18.6.4.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_6_4_3_force | <p>Whether to override the level requirement for CIS rule 18.6.4.3.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_6_4_4_enabled | <p>Whether to enable rule 18.6.4.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_netbios_dns_resolution_behavior | <p>The NetBIOS DNS resolution behavior.</p> | str | no | <ul><li>disabled_on_public_networks</li><li>disabled</li></ul> | disabled_on_public_networks |
| w2019cis_rule_18_6_5_1_enabled | <p>Whether to enable rule 18.6.5.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_6_5_1_force | <p>Whether to override the level requirement for CIS rule 18.6.5.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_6_8_1_enabled | <p>Whether to enable rule 18.6.8.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_6_9_1_enabled | <p>Whether to enable rule 18.6.9.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_6_9_1_force | <p>Whether to override the level requirement for CIS rule 18.6.9.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_6_9_2_enabled | <p>Whether to enable rule 18.6.9.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_6_9_2_force | <p>Whether to override the level requirement for CIS rule 18.6.9.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_6_10_2_enabled | <p>Whether to enable rule 18.6.10.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_6_10_2_force | <p>Whether to override the level requirement for CIS rule 18.6.10.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_6_11_2_enabled | <p>Whether to enable rule 18.6.11.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_6_11_3_enabled | <p>Whether to enable rule 18.6.11.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_6_11_4_enabled | <p>Whether to enable rule 18.6.11.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_6_14_1_enabled | <p>Whether to enable rule 18.6.14.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_6_19_2_1_enabled | <p>Whether to enable rule 18.6.19.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_6_19_2_1_force | <p>Whether to override the level requirement for CIS rule 18.6.19.2.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_6_20_1_enabled | <p>Whether to enable rule 18.6.20.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_6_20_1_force | <p>Whether to override the level requirement for CIS rule 18.6.20.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_6_20_2_enabled | <p>Whether to enable rule 18.6.20.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_6_20_2_force | <p>Whether to override the level requirement for CIS rule 18.6.20.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_6_21_1_enabled | <p>Whether to enable rule 18.6.21.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_6_21_2_enabled | <p>Whether to enable rule 18.6.21.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_6_21_2_force | <p>Whether to override the level requirement for CIS rule 18.6.21.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_7_1_enabled | <p>Whether to enable rule 18.7.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_7_1_force | <p>Whether to override the level requirement for CIS rule 18.7.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_7_2_enabled | <p>Whether to enable rule 18.7.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_7_3_enabled | <p>Whether to enable rule 18.7.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_7_4_enabled | <p>Whether to enable rule 18.7.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_7_5_enabled | <p>Whether to enable rule 18.7.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_7_6_enabled | <p>Whether to enable rule 18.7.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_7_7_enabled | <p>Whether to enable rule 18.7.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_7_8_enabled | <p>Whether to enable rule 18.7.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_7_9_enabled | <p>Whether to enable rule 18.7.9.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_7_10_enabled | <p>Whether to enable rule 18.7.10.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_7_11_enabled | <p>Whether to enable rule 18.7.11.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_7_12_enabled | <p>Whether to enable rule 18.7.12.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rpc_listener_authentication_protocol | <p>The RPC listener authentication protocol.</p> | str | no | <ul><li>negotiate</li><li>kerberos</li></ul> | negotiate |
| w2019cis_rule_18_8_1_1_enabled | <p>Whether to enable rule 18.8.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_8_1_1_force | <p>Whether to override the level requirement for CIS rule 18.8.1.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_9_3_1_enabled | <p>Whether to enable rule 18.9.3.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_4_1_enabled | <p>Whether to enable rule 18.9.4.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_4_2_enabled | <p>Whether to enable rule 18.9.4.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_5_1_enabled | <p>Whether to enable rule 18.9.5.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_5_1_force | <p>Whether to override the level requirement for CIS rule 18.9.5.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_9_5_2_enabled | <p>Whether to enable rule 18.9.5.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_5_2_force | <p>Whether to override the level requirement for CIS rule 18.9.5.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_9_5_3_enabled | <p>Whether to enable rule 18.9.5.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_5_3_force | <p>Whether to override the level requirement for CIS rule 18.9.5.3.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_9_5_4_enabled | <p>Whether to enable rule 18.9.5.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_5_4_force | <p>Whether to override the level requirement for CIS rule 18.9.5.4.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_9_5_5_enabled | <p>Whether to enable rule 18.9.5.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_5_5_force | <p>Whether to override the level requirement for CIS rule 18.9.5.5.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_9_5_6_enabled | <p>Whether to enable rule 18.9.5.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_5_6_force | <p>Whether to override the level requirement for CIS rule 18.9.5.6.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_9_5_7_enabled | <p>Whether to enable rule 18.9.5.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_5_7_force | <p>Whether to override the level requirement for CIS rule 18.9.5.7.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_vbs_platform_security_level | <p>The VBS platform security level.</p> | str | no | <ul><li>secure_boot</li><li>secure_boot_and_dma_protection</li></ul> | secure_boot |
| w2019cis_rule_18_9_7_2_enabled | <p>Whether to enable rule 18.9.7.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_13_1_enabled | <p>Whether to enable rule 18.9.13.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_19_2_enabled | <p>Whether to enable rule 18.9.19.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_19_3_enabled | <p>Whether to enable rule 18.9.19.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_19_4_enabled | <p>Whether to enable rule 18.9.19.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_19_5_enabled | <p>Whether to enable rule 18.9.19.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_19_6_enabled | <p>Whether to enable rule 18.9.19.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_19_7_enabled | <p>Whether to enable rule 18.9.19.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_20_1_1_enabled | <p>Whether to enable rule 18.9.20.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_20_1_2_enabled | <p>Whether to enable rule 18.9.20.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_20_1_2_force | <p>Whether to override the level requirement for CIS rule 18.9.20.1.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_9_20_1_3_enabled | <p>Whether to enable rule 18.9.20.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_20_1_3_force | <p>Whether to override the level requirement for CIS rule 18.9.20.1.3.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_9_20_1_4_enabled | <p>Whether to enable rule 18.9.20.1.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_20_1_4_force | <p>Whether to override the level requirement for CIS rule 18.9.20.1.4.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_9_20_1_5_enabled | <p>Whether to enable rule 18.9.20.1.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_20_1_6_enabled | <p>Whether to enable rule 18.9.20.1.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_20_1_6_force | <p>Whether to override the level requirement for CIS rule 18.9.20.1.6.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_9_20_1_7_enabled | <p>Whether to enable rule 18.9.20.1.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_20_1_7_force | <p>Whether to override the level requirement for CIS rule 18.9.20.1.7.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_9_20_1_8_enabled | <p>Whether to enable rule 18.9.20.1.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_20_1_8_force | <p>Whether to override the level requirement for CIS rule 18.9.20.1.8.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_9_20_1_9_enabled | <p>Whether to enable rule 18.9.20.1.9.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_20_1_9_force | <p>Whether to override the level requirement for CIS rule 18.9.20.1.9.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_9_20_1_10_enabled | <p>Whether to enable rule 18.9.20.1.10.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_20_1_10_force | <p>Whether to override the level requirement for CIS rule 18.9.20.1.10.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_9_20_1_11_enabled | <p>Whether to enable rule 18.9.20.1.11.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_20_1_11_force | <p>Whether to override the level requirement for CIS rule 18.9.20.1.11.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_9_20_1_12_enabled | <p>Whether to enable rule 18.9.20.1.12.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_20_1_12_force | <p>Whether to override the level requirement for CIS rule 18.9.20.1.12.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_9_20_1_13_enabled | <p>Whether to enable rule 18.9.20.1.13.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_20_1_13_force | <p>Whether to override the level requirement for CIS rule 18.9.20.1.13.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_9_23_1_enabled | <p>Whether to enable rule 18.9.23.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_23_1_force | <p>Whether to override the level requirement for CIS rule 18.9.23.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_9_24_1_enabled | <p>Whether to enable rule 18.9.24.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_25_1_enabled | <p>Whether to enable rule 18.9.25.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_25_2_enabled | <p>Whether to enable rule 18.9.25.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_25_3_enabled | <p>Whether to enable rule 18.9.25.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_25_4_enabled | <p>Whether to enable rule 18.9.25.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_25_5_enabled | <p>Whether to enable rule 18.9.25.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_25_6_enabled | <p>Whether to enable rule 18.9.25.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_25_7_enabled | <p>Whether to enable rule 18.9.25.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_25_8_enabled | <p>Whether to enable rule 18.9.25.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_laps_directory | <p>The directory in which to store LAPS passwords.</p> | str | no | <ul><li>azure_ad</li><li>ad</li></ul> | ad |
| w2019cis_laps_password_length | <p>The LAPS password length.</p> | int | no |  | 15 |
| w2019cis_laps_password_age_in_days | <p>The LAPS password age in days.</p> | int | no |  | 30 |
| w2019cis_laps_post_authentication_grace_period_in_hours | <p>The LAPS post-authentication grace period in hours.</p> | int | no |  | 8 |
| w2019cis_laps_post_authentication_actions | <p>The LAPS post-authentication actions to perform when the grace period expires.</p> | str | no | <ul><li>reset_password_and_logoff</li><li>reset_password_and_reboot</li></ul> | reset_password_and_logoff |
| w2019cis_rule_18_9_27_1_enabled | <p>Whether to enable rule 18.9.27.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_27_1_force | <p>Whether to override the level requirement for CIS rule 18.9.27.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_9_28_1_enabled | <p>Whether to enable rule 18.9.28.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_28_2_enabled | <p>Whether to enable rule 18.9.28.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_28_3_enabled | <p>Whether to enable rule 18.9.28.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_28_4_enabled | <p>Whether to enable rule 18.9.28.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_28_5_enabled | <p>Whether to enable rule 18.9.28.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_28_6_enabled | <p>Whether to enable rule 18.9.28.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_28_7_enabled | <p>Whether to enable rule 18.9.28.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_31_1_enabled | <p>Whether to enable rule 18.9.31.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_31_1_force | <p>Whether to override the level requirement for CIS rule 18.9.31.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_9_31_2_enabled | <p>Whether to enable rule 18.9.31.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_31_2_force | <p>Whether to override the level requirement for CIS rule 18.9.31.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_9_33_6_1_enabled | <p>Whether to enable rule 18.9.33.6.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_33_6_1_force | <p>Whether to override the level requirement for CIS rule 18.9.33.6.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_9_33_6_2_enabled | <p>Whether to enable rule 18.9.33.6.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_33_6_2_force | <p>Whether to override the level requirement for CIS rule 18.9.33.6.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_9_33_6_3_enabled | <p>Whether to enable rule 18.9.33.6.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_33_6_4_enabled | <p>Whether to enable rule 18.9.33.6.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_35_1_enabled | <p>Whether to enable rule 18.9.35.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_35_2_enabled | <p>Whether to enable rule 18.9.35.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_36_1_enabled | <p>Whether to enable rule 18.9.36.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_36_2_enabled | <p>Whether to enable rule 18.9.36.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_36_2_force | <p>Whether to override the level requirement for CIS rule 18.9.36.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_9_47_5_1_enabled | <p>Whether to enable rule 18.9.47.5.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_47_5_1_force | <p>Whether to override the level requirement for CIS rule 18.9.47.5.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_9_47_11_1_enabled | <p>Whether to enable rule 18.9.47.11.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_47_11_1_force | <p>Whether to override the level requirement for CIS rule 18.9.47.11.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_9_49_1_enabled | <p>Whether to enable rule 18.9.49.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_49_1_force | <p>Whether to override the level requirement for CIS rule 18.9.49.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_9_51_1_1_enabled | <p>Whether to enable rule 18.9.51.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_9_51_1_2_enabled | <p>Whether to enable rule 18.9.51.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_4_1_enabled | <p>Whether to enable rule 18.10.4.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_4_1_force | <p>Whether to override the level requirement for CIS rule 18.10.4.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_10_6_1_enabled | <p>Whether to enable rule 18.10.6.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_8_1_enabled | <p>Whether to enable rule 18.10.8.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_8_2_enabled | <p>Whether to enable rule 18.10.8.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_8_3_enabled | <p>Whether to enable rule 18.10.8.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_9_1_1_enabled | <p>Whether to enable rule 18.10.9.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_11_1_enabled | <p>Whether to enable rule 18.10.11.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_11_1_force | <p>Whether to override the level requirement for CIS rule 18.10.11.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_10_13_1_enabled | <p>Whether to enable rule 18.10.13.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_13_2_enabled | <p>Whether to enable rule 18.10.13.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_14_1_enabled | <p>Whether to enable rule 18.10.14.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_windows_connect_pin_requirement | <p>The Windows Connect PIN requirement.</p> | str | no | <ul><li>always</li><li>first_time</li></ul> | first_time |
| w2019cis_rule_18_10_15_1_enabled | <p>Whether to enable rule 18.10.15.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_15_2_enabled | <p>Whether to enable rule 18.10.15.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_16_1_enabled | <p>Whether to enable rule 18.10.16.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_16_2_enabled | <p>Whether to enable rule 18.10.16.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_16_2_force | <p>Whether to override the level requirement for CIS rule 18.10.16.8.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_10_16_3_enabled | <p>Whether to enable rule 18.10.16.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_16_4_enabled | <p>Whether to enable rule 18.10.16.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_16_5_enabled | <p>Whether to enable rule 18.10.16.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_16_6_enabled | <p>Whether to enable rule 18.10.16.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_16_7_enabled | <p>Whether to enable rule 18.10.16.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_allow_telemetry | <p>Whether to allow telemetry.</p> | str | no | <ul><li>required</li><li>off</li></ul> | off |
| w2019cis_rule_18_10_18_1_enabled | <p>Whether to enable rule 18.10.18.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_18_1_force | <p>Whether to override the level requirement for CIS rule 18.10.18.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_10_18_2_enabled | <p>Whether to enable rule 18.10.18.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_18_3_enabled | <p>Whether to enable rule 18.10.18.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_18_4_enabled | <p>Whether to enable rule 18.10.18.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_18_5_enabled | <p>Whether to enable rule 18.10.18.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_18_6_enabled | <p>Whether to enable rule 18.10.18.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_18_7_enabled | <p>Whether to enable rule 18.10.18.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_18_7_force | <p>Whether to override the level requirement for CIS rule 18.10.18.7.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_10_26_1_1_enabled | <p>Whether to enable rule 18.10.26.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_26_1_2_enabled | <p>Whether to enable rule 18.10.26.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_26_2_1_enabled | <p>Whether to enable rule 18.10.26.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_26_2_2_enabled | <p>Whether to enable rule 18.10.26.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_26_3_1_enabled | <p>Whether to enable rule 18.10.26.3.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_26_3_2_enabled | <p>Whether to enable rule 18.10.26.3.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_26_4_1_enabled | <p>Whether to enable rule 18.10.26.4.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_26_4_2_enabled | <p>Whether to enable rule 18.10.26.4.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_application_log_max_size_in_kb | <p>The maximum size of the Application log in KB.</p> | int | no |  | 32768 |
| w2019cis_security_log_max_size_in_kb | <p>The maximum size of the Security log in KB.</p> | int | no |  | 196608 |
| w2019cis_setup_log_max_size_in_kb | <p>The maximum size of the Setup log in KB.</p> | int | no |  | 32768 |
| w2019cis_system_log_max_size_in_kb | <p>The maximum size of the System log in KB.</p> | int | no |  | 32768 |
| w2019cis_rule_18_10_29_2_enabled | <p>Whether to enable rule 18.10.29.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_29_3_enabled | <p>Whether to enable rule 18.10.29.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_29_4_enabled | <p>Whether to enable rule 18.10.29.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_29_5_enabled | <p>Whether to enable rule 18.10.29.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_37_1_enabled | <p>Whether to enable rule 18.10.37.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_37_1_force | <p>Whether to override the level requirement for CIS rule 18.10.37.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_10_41_1_enabled | <p>Whether to enable rule 18.10.41.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_41_1_force | <p>Whether to override the level requirement for CIS rule 18.10.41.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_10_42_1_enabled | <p>Whether to enable rule 18.10.42.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_43_4_1_enabled | <p>Whether to enable rule 18.10.43.4.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_43_5_1_enabled | <p>Whether to enable rule 18.10.43.5.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_43_5_2_enabled | <p>Whether to enable rule 18.10.43.5.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_43_5_2_force | <p>Whether to override the level requirement for CIS rule 18.10.43.5.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_10_43_6_1_1_enabled | <p>Whether to enable rule 18.10.43.6.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_43_6_1_2_enabled | <p>Whether to enable rule 18.10.43.6.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_43_6_3_1_enabled | <p>Whether to enable rule 18.10.43.6.3.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_43_7_1_enabled | <p>Whether to enable rule 18.10.43.7.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_43_8_1_enabled | <p>Whether to enable rule 18.10.43.8.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_43_8_1_force | <p>Whether to override the level requirement for CIS rule 18.10.43.8.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_10_43_10_1_enabled | <p>Whether to enable rule 18.10.43.10.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_43_10_2_enabled | <p>Whether to enable rule 18.10.43.10.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_43_10_3_enabled | <p>Whether to enable rule 18.10.43.10.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_43_10_4_enabled | <p>Whether to enable rule 18.10.43.10.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_43_10_5_enabled | <p>Whether to enable rule 18.10.43.10.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_43_11_1_1_1_enabled | <p>Whether to enable rule 18.10.43.11.1.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_43_11_1_1_1_force | <p>Whether to override the level requirement for CIS rule 18.10.43.11.1.1.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_10_43_11_1_1_2_enabled | <p>Whether to enable rule 18.10.43.11.1.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_brute_force_protection_aggressiveness | <p>The aggressiveness of brute force protection.</p> | str | no | <ul><li>medium</li><li>high</li></ul> | medium |
| w2019cis_brute_force_protection_configured_state | <p>The configured state of brute force protection.</p> | str | no | <ul><li>audit</li><li>block</li></ul> | audit |
| w2019cis_rule_18_10_43_11_1_2_1_enabled | <p>Whether to enable rule 18.10.43.11.1.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_43_11_1_2_1_force | <p>Whether to override the level requirement for CIS rule 18.10.43.11.1.2.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_remote_encryption_protection_aggressiveness | <p>The aggressiveness of remote encryption protection.</p> | str | no | <ul><li>medium</li><li>high</li></ul> | medium |
| w2019cis_rule_18_10_43_12_1_enabled | <p>Whether to enable rule 18.10.43.12.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_43_12_1_force | <p>Whether to override the level requirement for CIS rule 18.10.43.12.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_10_43_13_1_enabled | <p>Whether to enable rule 18.10.43.13.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_43_13_2_enabled | <p>Whether to enable rule 18.10.43.13.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_43_13_3_enabled | <p>Whether to enable rule 18.10.43.13.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_43_13_4_enabled | <p>Whether to enable rule 18.10.43.13.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_43_13_5_enabled | <p>Whether to enable rule 18.10.43.13.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_43_16_enabled | <p>Whether to enable rule 18.10.43.16.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_43_17_enabled | <p>Whether to enable rule 18.10.43.17.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_51_1_enabled | <p>Whether to enable rule 18.10.51.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_56_1_enabled | <p>Whether to enable rule 18.10.56.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_56_1_force | <p>Whether to override the level requirement for CIS rule 18.10.56.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_10_57_2_2_enabled | <p>Whether to enable rule 18.10.57.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_57_3_2_1_enabled | <p>Whether to enable rule 18.10.57.3.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_57_3_2_1_force | <p>Whether to override the level requirement for CIS rule 18.10.57.3.2.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_10_57_3_3_1_enabled | <p>Whether to enable rule 18.10.57.3.3.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_57_3_3_1_force | <p>Whether to override the level requirement for CIS rule 18.10.57.3.3.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_10_57_3_3_2_enabled | <p>Whether to enable rule 18.10.57.3.3.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_57_3_3_3_enabled | <p>Whether to enable rule 18.10.57.3.3.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_57_3_3_3_force | <p>Whether to override the level requirement for CIS rule 18.10.57.3.3.3.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_10_57_3_3_4_enabled | <p>Whether to enable rule 18.10.57.3.3.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_57_3_3_4_force | <p>Whether to override the level requirement for CIS rule 18.10.57.3.3.4.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_10_57_3_9_1_enabled | <p>Whether to enable rule 18.10.57.3.9.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_57_3_9_2_enabled | <p>Whether to enable rule 18.10.57.3.9.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_57_3_9_3_enabled | <p>Whether to enable rule 18.10.57.3.9.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_57_3_9_4_enabled | <p>Whether to enable rule 18.10.57.3.9.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_57_3_9_5_enabled | <p>Whether to enable rule 18.10.57.3.9.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_57_3_10_1_enabled | <p>Whether to enable rule 18.10.57.3.10.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_57_3_10_1_force | <p>Whether to override the level requirement for CIS rule 18.10.57.3.10.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_10_57_3_10_2_enabled | <p>Whether to enable rule 18.10.57.3.10.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_57_3_10_2_force | <p>Whether to override the level requirement for CIS rule 18.10.57.3.10.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_10_57_3_11_1_enabled | <p>Whether to enable rule 18.10.57.3.11.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_57_3_11_2_enabled | <p>Whether to enable rule 18.10.57.3.11.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_remote_desktop_services_max_idle_time_in_ms | <p>The maximum idle time for Remote Desktop Services in milliseconds.</p> | int | no |  | 900000 |
| w2019cis_rule_18_10_58_1_enabled | <p>Whether to enable rule 18.10.58.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_58_2_enabled | <p>Whether to enable rule 18.10.58.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_59_2_enabled | <p>Whether to enable rule 18.10.59.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_59_2_force | <p>Whether to override the level requirement for CIS rule 18.10.59.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_10_59_3_enabled | <p>Whether to enable rule 18.10.59.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_59_4_enabled | <p>Whether to enable rule 18.10.59.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_63_1_enabled | <p>Whether to enable rule 18.10.63.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_63_1_force | <p>Whether to override the level requirement for CIS rule 18.10.63.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_10_76_2_1_enabled | <p>Whether to enable rule 18.10.76.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_80_1_enabled | <p>Whether to enable rule 18.10.80.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_80_1_force | <p>Whether to override the level requirement for CIS rule 18.10.80.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_10_80_2_enabled | <p>Whether to enable rule 18.10.80.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_windows_ink_workspace_access | <p>The Windows Ink Workspace access.</p> | str | no | <ul><li>disallow_above_lock</li><li>disabled</li></ul> | disallow_above_lock |
| w2019cis_rule_18_10_81_1_enabled | <p>Whether to enable rule 18.10.81.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_81_2_enabled | <p>Whether to enable rule 18.10.81.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_81_3_enabled | <p>Whether to enable rule 18.10.81.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_81_3_force | <p>Whether to override the level requirement for CIS rule 18.10.81.3.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_10_82_1_enabled | <p>Whether to enable rule 18.10.82.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_87_1_enabled | <p>Whether to enable rule 18.10.87.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_87_1_force | <p>Whether to override the level requirement for CIS rule 18.10.87.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_10_87_2_enabled | <p>Whether to enable rule 18.10.87.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_87_2_force | <p>Whether to override the level requirement for CIS rule 18.10.87.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_10_89_1_1_enabled | <p>Whether to enable rule 18.10.89.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_89_1_2_enabled | <p>Whether to enable rule 18.10.89.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_89_1_3_enabled | <p>Whether to enable rule 18.10.89.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_89_2_1_enabled | <p>Whether to enable rule 18.10.89.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_89_2_2_enabled | <p>Whether to enable rule 18.10.89.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_89_2_2_force | <p>Whether to override the level requirement for CIS rule 18.10.89.2.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_10_89_2_3_enabled | <p>Whether to enable rule 18.10.89.2.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_89_2_4_enabled | <p>Whether to enable rule 18.10.89.2.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_89_2_5_enabled | <p>Whether to enable rule 18.10.89.2.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_90_1_enabled | <p>Whether to enable rule 18.10.90.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_90_1_force | <p>Whether to override the level requirement for CIS rule 18.10.90.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_18_10_92_2_1_enabled | <p>Whether to enable rule 18.10.92.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_93_1_1_enabled | <p>Whether to enable rule 18.10.93.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_93_2_1_enabled | <p>Whether to enable rule 18.10.93.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_93_2_2_enabled | <p>Whether to enable rule 18.10.93.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_93_4_1_enabled | <p>Whether to enable rule 18.10.93.4.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_93_4_2_enabled | <p>Whether to enable rule 18.10.93.4.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_18_10_93_4_3_enabled | <p>Whether to enable rule 18.10.93.4.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_19_5_1_1_enabled | <p>Whether to enable rule 19.5.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_19_6_6_1_1_enabled | <p>Whether to enable rule 19.6.6.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_19_6_6_1_1_force | <p>Whether to override the level requirement for CIS rule 19.6.6.1.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_19_7_5_1_enabled | <p>Whether to enable rule 19.7.5.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_19_7_5_2_enabled | <p>Whether to enable rule 19.7.5.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_19_7_8_1_enabled | <p>Whether to enable rule 19.7.8.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_19_7_8_2_enabled | <p>Whether to enable rule 19.7.8.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_19_7_8_3_enabled | <p>Whether to enable rule 19.7.8.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_19_7_8_3_force | <p>Whether to override the level requirement for CIS rule 19.7.8.3.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_19_7_8_4_enabled | <p>Whether to enable rule 19.7.8.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_19_7_8_4_force | <p>Whether to override the level requirement for CIS rule 19.7.8.4.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w2019cis_rule_19_7_8_5_enabled | <p>Whether to enable rule 19.7.8.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_19_7_26_1_enabled | <p>Whether to enable rule 19.7.26.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_19_7_44_1_enabled | <p>Whether to enable rule 19.7.44.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_19_7_46_2_1_enabled | <p>Whether to enable rule 19.7.46.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w2019cis_rule_19_7_46_2_1_force | <p>Whether to override the level requirement for CIS rule 19.7.46.2.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |


## License
MIT

## Author and Project Information
Jim Tarpley (@trippsc2)
<!-- END_ANSIBLE_DOCS -->
