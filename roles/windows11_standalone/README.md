<!-- BEGIN_ANSIBLE_DOCS -->

# Ansible Role: trippsc2.cis.windows11_standalone
Version: 1.4.0

This role applies the CIS Benchmark hardening steps on standalone Windows 11 machines. It is based on the CIS Benchmark for Windows 11 Standalone, v5.0.0.


## Requirements

| Platform | Versions |
| -------- | -------- |
| Windows | <ul><li>all</li></ul> |

## Dependencies

| Collection |
| ---------- |
| ansible.windows |
| community.windows |

## Role Arguments
|Option|Description|Type|Required|Choices|Default|
|---|---|---|---|---|---|
| w11cis_skip_reboot | <p>Whether to skip the rebooting the machine.</p> | bool | no |  | False |
| w11cis_level | <p>The CIS Benchmark level to apply.</p> | int | no | <ul><li>1</li><li>2</li></ul> | 2 |
| w11cis_bitlocker | <p>Whether to apply the BitLocker rules.</p> | bool | no |  | True |
| w11cis_rule_1_1_1_enabled | <p>Whether to enable rule 1.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_1_1_2_enabled | <p>Whether to enable rule 1.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_1_1_3_enabled | <p>Whether to enable rule 1.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_1_1_4_enabled | <p>Whether to enable rule 1.1.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_1_1_5_enabled | <p>Whether to enable rule 1.1.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_1_1_6_enabled | <p>Whether to enable rule 1.1.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_1_1_7_enabled | <p>Whether to enable rule 1.1.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_password_history_size | <p>The number of passwords to remember.</p> | int | no |  | 24 |
| w11cis_maximum_password_age | <p>The maximum password age in days.</p> | int | no |  | 365 |
| w11cis_minimum_password_age | <p>The minimum password age in days.</p> | int | no |  | 1 |
| w11cis_minimum_password_length | <p>The minimum password length.</p> | int | no |  | 14 |
| w11cis_rule_1_2_1_enabled | <p>Whether to enable rule 1.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_1_2_2_enabled | <p>Whether to enable rule 1.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_1_2_3_enabled | <p>Whether to enable rule 1.2.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_1_2_4_enabled | <p>Whether to enable rule 1.2.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_lockout_duration_in_minutes | <p>The lockout duration in minutes.</p> | int | no |  | 15 |
| w11cis_lockout_bad_logon_count | <p>The number of bad logon attempts before lockout.</p> | int | no |  | 5 |
| w11cis_lockout_reset_time_in_minutes | <p>The lockout reset time in minutes.</p> | int | no |  | 15 |
| w11cis_rule_2_2_1_enabled | <p>Whether to enable rule 2.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_2_enabled | <p>Whether to enable rule 2.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_3_enabled | <p>Whether to enable rule 2.2.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_4_enabled | <p>Whether to enable rule 2.2.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_5_enabled | <p>Whether to enable rule 2.2.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_6_enabled | <p>Whether to enable rule 2.2.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_7_enabled | <p>Whether to enable rule 2.2.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_8_enabled | <p>Whether to enable rule 2.2.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_9_enabled | <p>Whether to enable rule 2.2.9.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_10_enabled | <p>Whether to enable rule 2.2.10.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_11_enabled | <p>Whether to enable rule 2.2.11.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_12_enabled | <p>Whether to enable rule 2.2.12.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_13_enabled | <p>Whether to enable rule 2.2.13.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_14_enabled | <p>Whether to enable rule 2.2.14.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_15_enabled | <p>Whether to enable rule 2.2.15.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_16_enabled | <p>Whether to enable rule 2.2.16.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_17_enabled | <p>Whether to enable rule 2.2.17.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_18_enabled | <p>Whether to enable rule 2.2.18.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_19_enabled | <p>Whether to enable rule 2.2.19.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_20_enabled | <p>Whether to enable rule 2.2.20.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_21_enabled | <p>Whether to enable rule 2.2.21.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_22_enabled | <p>Whether to enable rule 2.2.22.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_23_enabled | <p>Whether to enable rule 2.2.23.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_24_enabled | <p>Whether to enable rule 2.2.24.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_25_enabled | <p>Whether to enable rule 2.2.25.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_26_enabled | <p>Whether to enable rule 2.2.26.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_27_enabled | <p>Whether to enable rule 2.2.27.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_27_force | <p>Whether to override the level requirement for CIS rule 2.2.27.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_2_2_28_enabled | <p>Whether to enable rule 2.2.28.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_28_force | <p>Whether to override the level requirement for CIS rule 2.2.28.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_2_2_29_enabled | <p>Whether to enable rule 2.2.29.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_30_enabled | <p>Whether to enable rule 2.2.30.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_31_enabled | <p>Whether to enable rule 2.2.31.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_32_enabled | <p>Whether to enable rule 2.2.32.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_33_enabled | <p>Whether to enable rule 2.2.33.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_34_enabled | <p>Whether to enable rule 2.2.34.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_35_enabled | <p>Whether to enable rule 2.2.35.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_36_enabled | <p>Whether to enable rule 2.2.36.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_37_enabled | <p>Whether to enable rule 2.2.37.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_2_38_enabled | <p>Whether to enable rule 2.2.38.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_access_this_computer_from_the_network_additional_users | <p>Additional users to grant `Access this computer from the network` permissions.</p> | list of 'str' | no |  | [] |
| w11cis_adjust_memory_quotas_for_a_process_additional_users | <p>Additional users to grant `Adjust memory quotas for a process` permissions.</p> | list of 'str' | no |  | [] |
| w11cis_create_global_objects_additional_users | <p>Additional users to grant `Create global objects` permissions.</p> | list of 'str' | no |  | [] |
| w11cis_debug_programs_additional_users | <p>Additional users to grant `Debug programs` permissions.</p> | list of 'str' | no |  | [] |
| w11cis_generate_security_audits_additional_users | <p>Additional users to grant `Generate security audits` permissions.</p> | list of 'str' | no |  | [] |
| w11cis_impersonate_a_client_after_authentication_additional_users | <p>Additional users to grant `Impersonate a client after authentication` permissions.</p> | list of 'str' | no |  | [] |
| w11cis_perform_volume_maintenance_tasks_additional_users | <p>Additional users to grant `Perform volume maintenance tasks` permissions.</p> | list of 'str' | no |  | [] |
| w11cis_replace_a_process_level_token_additional_users | <p>Additional users to grant `Replace a process level token` permissions.</p> | list of 'str' | no |  | [] |
| w11cis_rule_2_3_1_1_enabled | <p>Whether to enable rule 2.3.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_1_2_enabled | <p>Whether to enable rule 2.3.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_1_3_enabled | <p>Whether to enable rule 2.3.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_1_4_enabled | <p>Whether to enable rule 2.3.1.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_admin_username | <p>The name to which to set the default Administrator account.</p> | str | no |  |  |
| w11cis_guest_username | <p>The name to which to set the default Guest account.</p> | str | no |  |  |
| w11cis_rule_2_3_2_1_enabled | <p>Whether to enable rule 2.3.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_2_2_enabled | <p>Whether to enable rule 2.3.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_4_1_enabled | <p>Whether to enable rule 2.3.4.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_4_1_force | <p>Whether to override the level requirement for CIS rule 2.3.4.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_2_3_7_1_enabled | <p>Whether to enable rule 2.3.7.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_7_1_force | <p>Whether to override the level requirement for CIS rule 2.3.7.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_2_3_7_2_enabled | <p>Whether to enable rule 2.3.7.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_7_3_enabled | <p>Whether to enable rule 2.3.7.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_7_4_enabled | <p>Whether to enable rule 2.3.7.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_7_5_enabled | <p>Whether to enable rule 2.3.7.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_7_6_enabled | <p>Whether to enable rule 2.3.7.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_7_7_enabled | <p>Whether to enable rule 2.3.7.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_inactivity_timeout_in_seconds | <p>The inactivity timeout in seconds.</p> | int | no |  | 900 |
| w11cis_login_message_text | <p>The legal notice text.</p> | str | no |  |  |
| w11cis_login_message_title | <p>The legal notice caption.</p> | str | no |  |  |
| w11cis_password_expiry_warning_in_days | <p>The password expiry warning in days.</p> | int | no |  | 14 |
| w11cis_smart_card_removal_behavior | <p>The smart card removal behavior.</p> | str | no | <ul><li>lock</li><li>logoff</li><li>disconnect</li></ul> | lock |
| w11cis_rule_2_3_8_1_enabled | <p>Whether to enable rule 2.3.8.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_8_2_enabled | <p>Whether to enable rule 2.3.8.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_9_1_enabled | <p>Whether to enable rule 2.3.9.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_9_2_enabled | <p>Whether to enable rule 2.3.9.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_9_3_enabled | <p>Whether to enable rule 2.3.9.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_9_4_enabled | <p>Whether to enable rule 2.3.9.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_idle_smb_timeout_in_minutes | <p>The idle SMB timeout in minutes.</p> | int | no |  | 15 |
| w11cis_smb_spn_target_name_validation_level | <p>The SMB SPN target name validation level.</p> | str | no | <ul><li>accept</li><li>required</li></ul> | required |
| w11cis_rule_2_3_10_1_enabled | <p>Whether to enable rule 2.3.10.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_10_2_enabled | <p>Whether to enable rule 2.3.10.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_10_3_enabled | <p>Whether to enable rule 2.3.10.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_10_4_enabled | <p>Whether to enable rule 2.3.10.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_10_5_enabled | <p>Whether to enable rule 2.3.10.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_10_6_enabled | <p>Whether to enable rule 2.3.10.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_10_7_enabled | <p>Whether to enable rule 2.3.10.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_10_8_enabled | <p>Whether to enable rule 2.3.10.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_10_9_enabled | <p>Whether to enable rule 2.3.10.9.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_10_10_enabled | <p>Whether to enable rule 2.3.10.10.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_10_11_enabled | <p>Whether to enable rule 2.3.10.11.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_10_12_enabled | <p>Whether to enable rule 2.3.10.12.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_null_session_pipes | <p>The null session pipes.</p> | list of 'str' | no |  | [] |
| w11cis_remote_registry_paths | <p>The remote registry paths.</p> | list of 'str' | no |  | ['System\\CurrentControlSet\\Control\\Print\\Printers', 'System\\CurrentControlSet\\Services\\Eventlog', 'Software\\Microsoft\\OLAP Server', 'Software\\Microsoft\\Windows NT\\CurrentVersion\\Print', 'Software\\Microsoft\\Windows NT\\CurrentVersion\\Windows', 'System\\CurrentControlSet\\Control\\ContentIndex', 'System\\CurrentControlSet\\Control\\Terminal Server', 'System\\CurrentControlSet\\Control\\Terminal Server\\UserConfig', 'System\\CurrentControlSet\\Control\\Terminal Server\\DefaultUserConfiguration', 'Software\\Microsoft\\Windows NT\\CurrentVersion\\Perflib', 'System\\CurrentControlSet\\Services\\SysmonLog'] |
| w11cis_rule_2_3_11_1_enabled | <p>Whether to enable rule 2.3.11.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_11_2_enabled | <p>Whether to enable rule 2.3.11.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_11_3_enabled | <p>Whether to enable rule 2.3.11.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_11_4_enabled | <p>Whether to enable rule 2.3.11.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_11_5_enabled | <p>Whether to enable rule 2.3.11.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_11_6_enabled | <p>Whether to enable rule 2.3.11.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_11_7_enabled | <p>Whether to enable rule 2.3.11.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_11_8_enabled | <p>Whether to enable rule 2.3.11.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_11_9_enabled | <p>Whether to enable rule 2.3.11.9.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_11_10_enabled | <p>Whether to enable rule 2.3.11.10.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_11_11_enabled | <p>Whether to enable rule 2.3.11.11.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_11_12_enabled | <p>Whether to enable rule 2.3.11.12.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_ldap_client_encryption_requirements | <p>The LDAP client encryption requirements.</p> | str | no | <ul><li>require</li><li>negotiate</li></ul> | negotiate |
| w11cis_ldap_client_signing_requirements | <p>The LDAP client signing requirements.</p> | str | no | <ul><li>require</li><li>negotiate</li></ul> | require |
| w11cis_outgoing_ntlm_traffic_requirement | <p>The outgoing NTLM traffic requirement.</p> | str | no | <ul><li>audit_all</li><li>deny_all</li></ul> | audit_all |
| w11cis_rule_2_3_14_1_enabled | <p>Whether to enable rule 2.3.14.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_14_1_force | <p>Whether to override the level requirement for CIS rule 2.3.14.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_private_key_prompt | <p>The prompt behavior for private S-MIME key use.</p> | str | no | <ul><li>prompt_first_use</li><li>prompt_always</li></ul> | prompt_first_use |
| w11cis_rule_2_3_15_1_enabled | <p>Whether to enable rule 2.3.15.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_15_2_enabled | <p>Whether to enable rule 2.3.15.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_17_1_enabled | <p>Whether to enable rule 2.3.17.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_17_2_enabled | <p>Whether to enable rule 2.3.17.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_17_3_enabled | <p>Whether to enable rule 2.3.17.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_17_4_enabled | <p>Whether to enable rule 2.3.17.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_17_5_enabled | <p>Whether to enable rule 2.3.17.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_17_6_enabled | <p>Whether to enable rule 2.3.17.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_17_7_enabled | <p>Whether to enable rule 2.3.17.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_2_3_17_8_enabled | <p>Whether to enable rule 2.3.17.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_admin_uac_elevation_behavior | <p>The UAC elevation behavior for administrators.</p> | str | no | <ul><li>prompt_for_credentials</li><li>prompt_for_consent</li></ul> | prompt_for_consent |
| w11cis_rule_5_1_enabled | <p>Whether to enable rule 5.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_1_force | <p>Whether to override the level requirement for CIS rule 5.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_5_2_enabled | <p>Whether to enable rule 5.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_2_force | <p>Whether to override the level requirement for CIS rule 5.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_5_3_enabled | <p>Whether to enable rule 5.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_4_enabled | <p>Whether to enable rule 5.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_4_force | <p>Whether to override the level requirement for CIS rule 5.4.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_5_5_enabled | <p>Whether to enable rule 5.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_5_force | <p>Whether to override the level requirement for CIS rule 5.5.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_5_6_enabled | <p>Whether to enable rule 5.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_6_force | <p>Whether to override the level requirement for CIS rule 5.6.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_5_7_enabled | <p>Whether to enable rule 5.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_8_enabled | <p>Whether to enable rule 5.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_9_enabled | <p>Whether to enable rule 5.9.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_9_force | <p>Whether to override the level requirement for CIS rule 5.9.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_5_10_enabled | <p>Whether to enable rule 5.10.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_11_enabled | <p>Whether to enable rule 5.11.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_11_force | <p>Whether to override the level requirement for CIS rule 5.11.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_5_12_enabled | <p>Whether to enable rule 5.12.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_13_enabled | <p>Whether to enable rule 5.13.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_13_force | <p>Whether to override the level requirement for CIS rule 5.13.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_5_14_enabled | <p>Whether to enable rule 5.14.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_14_force | <p>Whether to override the level requirement for CIS rule 5.14.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_5_15_enabled | <p>Whether to enable rule 5.15.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_15_force | <p>Whether to override the level requirement for CIS rule 5.15.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_5_16_enabled | <p>Whether to enable rule 5.16.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_16_force | <p>Whether to override the level requirement for CIS rule 5.16.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_5_17_enabled | <p>Whether to enable rule 5.17.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_17_force | <p>Whether to override the level requirement for CIS rule 5.17.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_5_18_enabled | <p>Whether to enable rule 5.18.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_18_force | <p>Whether to override the level requirement for CIS rule 5.18.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_5_19_enabled | <p>Whether to enable rule 5.19.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_19_force | <p>Whether to override the level requirement for CIS rule 5.19.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_5_20_enabled | <p>Whether to enable rule 5.20.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_20_force | <p>Whether to override the level requirement for CIS rule 5.20.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_5_21_enabled | <p>Whether to enable rule 5.21.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_21_force | <p>Whether to override the level requirement for CIS rule 5.21.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_5_22_enabled | <p>Whether to enable rule 5.22.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_22_force | <p>Whether to override the level requirement for CIS rule 5.22.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_5_23_enabled | <p>Whether to enable rule 5.23.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_24_enabled | <p>Whether to enable rule 5.24.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_24_force | <p>Whether to override the level requirement for CIS rule 5.24.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_5_25_enabled | <p>Whether to enable rule 5.25.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_26_enabled | <p>Whether to enable rule 5.26.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_26_force | <p>Whether to override the level requirement for CIS rule 5.26.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_5_27_enabled | <p>Whether to enable rule 5.27.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_28_enabled | <p>Whether to enable rule 5.28.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_28_force | <p>Whether to override the level requirement for CIS rule 5.28.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_5_29_enabled | <p>Whether to enable rule 5.29.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_30_enabled | <p>Whether to enable rule 5.30.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_31_enabled | <p>Whether to enable rule 5.31.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_32_enabled | <p>Whether to enable rule 5.32.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_33_enabled | <p>Whether to enable rule 5.33.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_33_force | <p>Whether to override the level requirement for CIS rule 5.33.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_5_34_enabled | <p>Whether to enable rule 5.34.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_34_force | <p>Whether to override the level requirement for CIS rule 5.34.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_5_35_enabled | <p>Whether to enable rule 5.35.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_36_enabled | <p>Whether to enable rule 5.36.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_37_enabled | <p>Whether to enable rule 5.37.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_37_force | <p>Whether to override the level requirement for CIS rule 5.37.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_5_38_enabled | <p>Whether to enable rule 5.38.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_38_force | <p>Whether to override the level requirement for CIS rule 5.38.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_5_39_enabled | <p>Whether to enable rule 5.39.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_39_force | <p>Whether to override the level requirement for CIS rule 5.39.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_5_40_enabled | <p>Whether to enable rule 5.40.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_41_enabled | <p>Whether to enable rule 5.41.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_42_enabled | <p>Whether to enable rule 5.42.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_43_enabled | <p>Whether to enable rule 5.43.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_5_44_enabled | <p>Whether to enable rule 5.44.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_9_2_1_enabled | <p>Whether to enable rule 9.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_9_2_2_enabled | <p>Whether to enable rule 9.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_9_2_3_enabled | <p>Whether to enable rule 9.2.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_9_2_4_enabled | <p>Whether to enable rule 9.2.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_9_2_5_enabled | <p>Whether to enable rule 9.2.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_9_2_6_enabled | <p>Whether to enable rule 9.2.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_9_2_7_enabled | <p>Whether to enable rule 9.2.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_private_firewall_log_path | <p>The path to the private firewall log.</p> | str | no |  | %SystemRoot%\System32\logfiles\firewall\privatefw.log |
| w11cis_private_firewall_log_size_in_kb | <p>The size of the private firewall log in KB.</p> | int | no |  | 16384 |
| w11cis_rule_9_3_1_enabled | <p>Whether to enable rule 9.3.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_9_3_2_enabled | <p>Whether to enable rule 9.3.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_9_3_3_enabled | <p>Whether to enable rule 9.3.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_9_3_4_enabled | <p>Whether to enable rule 9.3.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_9_3_5_enabled | <p>Whether to enable rule 9.3.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_9_3_6_enabled | <p>Whether to enable rule 9.3.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_9_3_7_enabled | <p>Whether to enable rule 9.3.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_public_firewall_log_path | <p>The path to the public firewall log.</p> | str | no |  | %SystemRoot%\System32\logfiles\firewall\publicfw.log |
| w11cis_public_firewall_log_size_in_kb | <p>The size of the public firewall log in KB.</p> | int | no |  | 16384 |
| w11cis_rule_17_1_1_enabled | <p>Whether to enable rule 17.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_17_2_1_enabled | <p>Whether to enable rule 17.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_17_2_2_enabled | <p>Whether to enable rule 17.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_17_2_3_enabled | <p>Whether to enable rule 17.2.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_17_3_1_enabled | <p>Whether to enable rule 17.3.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_17_3_2_enabled | <p>Whether to enable rule 17.3.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_17_5_1_enabled | <p>Whether to enable rule 17.5.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_17_5_2_enabled | <p>Whether to enable rule 17.5.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_17_5_3_enabled | <p>Whether to enable rule 17.5.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_17_5_4_enabled | <p>Whether to enable rule 17.5.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_17_5_5_enabled | <p>Whether to enable rule 17.5.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_17_5_6_enabled | <p>Whether to enable rule 17.5.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_17_6_1_enabled | <p>Whether to enable rule 17.6.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_17_6_2_enabled | <p>Whether to enable rule 17.6.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_17_6_3_enabled | <p>Whether to enable rule 17.6.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_17_6_4_enabled | <p>Whether to enable rule 17.6.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_17_7_1_enabled | <p>Whether to enable rule 17.7.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_17_7_2_enabled | <p>Whether to enable rule 17.7.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_17_7_3_enabled | <p>Whether to enable rule 17.7.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_17_7_4_enabled | <p>Whether to enable rule 17.7.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_17_7_5_enabled | <p>Whether to enable rule 17.7.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_17_8_1_enabled | <p>Whether to enable rule 17.8.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_17_9_1_enabled | <p>Whether to enable rule 17.9.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_17_9_2_enabled | <p>Whether to enable rule 17.9.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_17_9_3_enabled | <p>Whether to enable rule 17.9.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_17_9_4_enabled | <p>Whether to enable rule 17.9.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_17_9_5_enabled | <p>Whether to enable rule 17.9.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_1_1_1_enabled | <p>Whether to enable rule 18.1.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_1_1_2_enabled | <p>Whether to enable rule 18.1.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_1_2_2_enabled | <p>Whether to enable rule 18.1.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_1_3_enabled | <p>Whether to enable rule 18.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_1_3_force | <p>Whether to override the level requirement for CIS rule 18.1.3.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_4_1_enabled | <p>Whether to enable rule 18.4.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_4_2_enabled | <p>Whether to enable rule 18.4.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_4_3_enabled | <p>Whether to enable rule 18.4.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_4_4_enabled | <p>Whether to enable rule 18.4.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_4_5_enabled | <p>Whether to enable rule 18.4.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_4_6_enabled | <p>Whether to enable rule 18.4.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_5_1_enabled | <p>Whether to enable rule 18.5.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_5_2_enabled | <p>Whether to enable rule 18.5.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_5_3_enabled | <p>Whether to enable rule 18.5.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_5_4_enabled | <p>Whether to enable rule 18.5.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_5_4_force | <p>Whether to override the level requirement for CIS rule 18.5.4.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_5_5_enabled | <p>Whether to enable rule 18.5.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_5_6_enabled | <p>Whether to enable rule 18.5.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_5_6_force | <p>Whether to override the level requirement for CIS rule 18.5.6.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_5_7_enabled | <p>Whether to enable rule 18.5.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_5_8_enabled | <p>Whether to enable rule 18.5.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_5_8_force | <p>Whether to override the level requirement for CIS rule 18.5.8.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_5_9_enabled | <p>Whether to enable rule 18.5.9.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_5_10_enabled | <p>Whether to enable rule 18.5.10.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_5_10_force | <p>Whether to override the level requirement for CIS rule 18.5.10.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_5_11_enabled | <p>Whether to enable rule 18.5.11.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_5_11_force | <p>Whether to override the level requirement for CIS rule 18.5.11.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_5_12_enabled | <p>Whether to enable rule 18.5.12.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_security_log_warning_level | <p>The percentage of the security log that must be filled before a warning event is generated.</p> | int | no |  | 90 |
| w11cis_rule_18_6_4_1_enabled | <p>Whether to enable rule 18.6.4.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_6_4_2_enabled | <p>Whether to enable rule 18.6.4.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_6_4_2_force | <p>Whether to override the level requirement for CIS rule 18.6.4.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_6_5_1_enabled | <p>Whether to enable rule 18.6.5.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_6_5_1_force | <p>Whether to override the level requirement for CIS rule 18.6.5.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_6_7_1_enabled | <p>Whether to enable rule 18.6.7.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_6_7_2_enabled | <p>Whether to enable rule 18.6.7.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_6_7_3_enabled | <p>Whether to enable rule 18.6.7.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_6_7_4_enabled | <p>Whether to enable rule 18.6.7.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_6_7_5_enabled | <p>Whether to enable rule 18.6.7.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_6_7_6_enabled | <p>Whether to enable rule 18.6.7.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_6_7_7_enabled | <p>Whether to enable rule 18.6.7.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_smb_authentication_rate_limiter_delay_in_ms | <p>The SMB authentication rate limiter delay in milliseconds.</p> | int | no |  | 2000 |
| w11cis_rule_18_6_8_1_enabled | <p>Whether to enable rule 18.6.8.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_6_8_2_enabled | <p>Whether to enable rule 18.6.8.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_6_8_3_enabled | <p>Whether to enable rule 18.6.8.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_6_8_4_enabled | <p>Whether to enable rule 18.6.8.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_6_8_5_enabled | <p>Whether to enable rule 18.6.8.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_6_8_6_enabled | <p>Whether to enable rule 18.6.8.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_6_8_7_enabled | <p>Whether to enable rule 18.6.8.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_6_9_1_enabled | <p>Whether to enable rule 18.6.9.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_6_9_1_force | <p>Whether to override the level requirement for CIS rule 18.6.9.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_6_9_2_enabled | <p>Whether to enable rule 18.6.9.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_6_9_2_force | <p>Whether to override the level requirement for CIS rule 18.6.9.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_6_10_2_enabled | <p>Whether to enable rule 18.6.10.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_6_10_2_force | <p>Whether to override the level requirement for CIS rule 18.6.10.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_6_11_2_enabled | <p>Whether to enable rule 18.6.11.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_6_11_3_enabled | <p>Whether to enable rule 18.6.11.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_6_14_1_enabled | <p>Whether to enable rule 18.6.14.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_6_19_2_1_enabled | <p>Whether to enable rule 18.6.19.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_6_19_2_1_force | <p>Whether to override the level requirement for CIS rule 18.6.19.2.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_6_20_1_enabled | <p>Whether to enable rule 18.6.20.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_6_20_1_force | <p>Whether to override the level requirement for CIS rule 18.6.20.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_6_20_2_enabled | <p>Whether to enable rule 18.6.20.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_6_20_2_force | <p>Whether to override the level requirement for CIS rule 18.6.20.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_6_21_1_enabled | <p>Whether to enable rule 18.6.21.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_6_23_2_1_enabled | <p>Whether to enable rule 18.6.23.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_7_1_enabled | <p>Whether to enable rule 18.7.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_7_1_force | <p>Whether to override the level requirement for CIS rule 18.7.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_7_2_enabled | <p>Whether to enable rule 18.7.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_7_3_enabled | <p>Whether to enable rule 18.7.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_7_4_enabled | <p>Whether to enable rule 18.7.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_7_5_enabled | <p>Whether to enable rule 18.7.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_7_6_enabled | <p>Whether to enable rule 18.7.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_7_7_enabled | <p>Whether to enable rule 18.7.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_7_8_enabled | <p>Whether to enable rule 18.7.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_7_9_enabled | <p>Whether to enable rule 18.7.9.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_7_9_force | <p>Whether to override the level requirement for CIS rule 18.7.9.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_7_10_enabled | <p>Whether to enable rule 18.7.10.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_7_11_enabled | <p>Whether to enable rule 18.7.11.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_7_12_enabled | <p>Whether to enable rule 18.7.12.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_7_13_enabled | <p>Whether to enable rule 18.7.13.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_7_14_enabled | <p>Whether to enable rule 18.7.14.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_7_14_force | <p>Whether to override the level requirement for CIS rule 18.7.14.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_7_15_enabled | <p>Whether to enable rule 18.7.15.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_7_15_force | <p>Whether to override the level requirement for CIS rule 18.7.15.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_7_16_enabled | <p>Whether to enable rule 18.7.16.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_7_16_force | <p>Whether to override the level requirement for CIS rule 18.7.16.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_7_17_enabled | <p>Whether to enable rule 18.7.17.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_7_17_force | <p>Whether to override the level requirement for CIS rule 18.7.17.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_7_18_enabled | <p>Whether to enable rule 18.7.18.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_7_18_force | <p>Whether to override the level requirement for CIS rule 18.7.18.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rpc_listener_authentication_protocol | <p>The RPC listener authentication protocol.</p> | str | no | <ul><li>negotiate</li><li>kerberos</li></ul> | negotiate |
| w11cis_rule_18_8_1_1_enabled | <p>Whether to enable rule 18.8.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_8_1_1_force | <p>Whether to override the level requirement for CIS rule 18.8.1.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_8_1_2_enabled | <p>Whether to enable rule 18.8.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_8_1_2_force | <p>Whether to override the level requirement for CIS rule 18.8.1.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_9_3_1_enabled | <p>Whether to enable rule 18.9.3.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_4_1_enabled | <p>Whether to enable rule 18.9.4.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_4_2_enabled | <p>Whether to enable rule 18.9.4.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_5_1_enabled | <p>Whether to enable rule 18.9.5.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_5_2_enabled | <p>Whether to enable rule 18.9.5.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_5_3_enabled | <p>Whether to enable rule 18.9.5.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_5_4_enabled | <p>Whether to enable rule 18.9.5.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_5_5_enabled | <p>Whether to enable rule 18.9.5.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_5_6_enabled | <p>Whether to enable rule 18.9.5.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_5_7_enabled | <p>Whether to enable rule 18.9.5.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_vbs_platform_security_level | <p>The VBS platform security level.</p> | str | no | <ul><li>secure_boot</li><li>secure_boot_and_dma_protection</li></ul> | secure_boot |
| w11cis_rule_18_9_7_1_1_enabled | <p>Whether to enable rule 18.9.7.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_7_1_1_force | <p>Whether to override the level requirement for CIS rule 18.9.7.1.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_9_7_1_2_enabled | <p>Whether to enable rule 18.9.7.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_7_1_2_force | <p>Whether to override the level requirement for CIS rule 18.9.7.1.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_9_7_1_3_enabled | <p>Whether to enable rule 18.9.7.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_7_1_3_force | <p>Whether to override the level requirement for CIS rule 18.9.7.1.3.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_9_7_2_enabled | <p>Whether to enable rule 18.9.7.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_13_1_enabled | <p>Whether to enable rule 18.9.13.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_17_1_enabled | <p>Whether to enable rule 18.9.17.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_19_2_enabled | <p>Whether to enable rule 18.9.19.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_20_1_1_enabled | <p>Whether to enable rule 18.9.20.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_20_1_1_force | <p>Whether to override the level requirement for CIS rule 18.9.20.1.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_9_20_1_2_enabled | <p>Whether to enable rule 18.9.20.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_20_1_3_enabled | <p>Whether to enable rule 18.9.20.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_20_1_3_force | <p>Whether to override the level requirement for CIS rule 18.9.20.1.3.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_9_20_1_4_enabled | <p>Whether to enable rule 18.9.20.1.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_20_1_4_force | <p>Whether to override the level requirement for CIS rule 18.9.20.1.4.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_9_20_1_5_enabled | <p>Whether to enable rule 18.9.20.1.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_20_1_5_force | <p>Whether to override the level requirement for CIS rule 18.9.20.1.5.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_9_20_1_6_enabled | <p>Whether to enable rule 18.9.20.1.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_20_1_7_enabled | <p>Whether to enable rule 18.9.20.1.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_20_1_7_force | <p>Whether to override the level requirement for CIS rule 18.9.20.1.7.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_9_20_1_8_enabled | <p>Whether to enable rule 18.9.20.1.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_20_1_8_force | <p>Whether to override the level requirement for CIS rule 18.9.20.1.8.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_9_20_1_9_enabled | <p>Whether to enable rule 18.9.20.1.9.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_20_1_9_force | <p>Whether to override the level requirement for CIS rule 18.9.20.1.9.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_9_20_1_10_enabled | <p>Whether to enable rule 18.9.20.1.10.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_20_1_10_force | <p>Whether to override the level requirement for CIS rule 18.9.20.1.10.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_9_20_1_11_enabled | <p>Whether to enable rule 18.9.20.1.11.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_20_1_11_force | <p>Whether to override the level requirement for CIS rule 18.9.20.1.11.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_9_20_1_12_enabled | <p>Whether to enable rule 18.9.20.1.12.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_20_1_12_force | <p>Whether to override the level requirement for CIS rule 18.9.20.1.12.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_9_20_1_13_enabled | <p>Whether to enable rule 18.9.20.1.13.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_20_1_13_force | <p>Whether to override the level requirement for CIS rule 18.9.20.1.13.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_9_20_1_14_enabled | <p>Whether to enable rule 18.9.20.1.14.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_20_1_14_force | <p>Whether to override the level requirement for CIS rule 18.9.20.1.14.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_9_23_1_enabled | <p>Whether to enable rule 18.9.23.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_23_1_force | <p>Whether to override the level requirement for CIS rule 18.9.23.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_9_24_1_enabled | <p>Whether to enable rule 18.9.24.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_24_1_force | <p>Whether to override the level requirement for CIS rule 18.9.24.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_9_27_1_enabled | <p>Whether to enable rule 18.9.27.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_27_2_enabled | <p>Whether to enable rule 18.9.27.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_28_1_enabled | <p>Whether to enable rule 18.9.28.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_28_1_force | <p>Whether to override the level requirement for CIS rule 18.9.28.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_9_29_1_enabled | <p>Whether to enable rule 18.9.29.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_29_2_enabled | <p>Whether to enable rule 18.9.29.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_29_3_enabled | <p>Whether to enable rule 18.9.29.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_29_4_enabled | <p>Whether to enable rule 18.9.29.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_33_1_enabled | <p>Whether to enable rule 18.9.33.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_33_1_force | <p>Whether to override the level requirement for CIS rule 18.9.33.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_9_33_2_enabled | <p>Whether to enable rule 18.9.33.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_33_2_force | <p>Whether to override the level requirement for CIS rule 18.9.33.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_9_35_1_enabled | <p>Whether to enable rule 18.9.35.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_35_2_enabled | <p>Whether to enable rule 18.9.35.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_35_3_enabled | <p>Whether to enable rule 18.9.35.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_35_3_force | <p>Whether to override the level requirement for CIS rule 18.9.35.3.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_9_35_4_enabled | <p>Whether to enable rule 18.9.35.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_35_4_force | <p>Whether to override the level requirement for CIS rule 18.9.35.4.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_9_35_5_enabled | <p>Whether to enable rule 18.9.35.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_35_6_enabled | <p>Whether to enable rule 18.9.35.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_37_1_enabled | <p>Whether to enable rule 18.9.37.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_37_2_enabled | <p>Whether to enable rule 18.9.37.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_38_1_enabled | <p>Whether to enable rule 18.9.38.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_38_2_enabled | <p>Whether to enable rule 18.9.38.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_49_5_1_enabled | <p>Whether to enable rule 18.9.49.5.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_49_5_1_force | <p>Whether to override the level requirement for CIS rule 18.9.49.5.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_9_49_11_1_enabled | <p>Whether to enable rule 18.9.49.11.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_49_11_1_force | <p>Whether to override the level requirement for CIS rule 18.9.49.11.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_9_51_1_enabled | <p>Whether to enable rule 18.9.51.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_51_1_force | <p>Whether to override the level requirement for CIS rule 18.9.51.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_9_53_1_1_enabled | <p>Whether to enable rule 18.9.53.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_9_54_enabled | <p>Whether to enable rule 18.9.54.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_3_1_enabled | <p>Whether to enable rule 18.10.3.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_3_1_force | <p>Whether to override the level requirement for CIS rule 18.10.3.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_3_2_enabled | <p>Whether to enable rule 18.10.3.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_3_2_force | <p>Whether to override the level requirement for CIS rule 18.10.3.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_3_3_enabled | <p>Whether to enable rule 18.10.3.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_3_3_force | <p>Whether to override the level requirement for CIS rule 18.10.3.3.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_4_1_enabled | <p>Whether to enable rule 18.10.4.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_4_1_force | <p>Whether to override the level requirement for CIS rule 18.10.4.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_4_2_enabled | <p>Whether to enable rule 18.10.4.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_4_3_enabled | <p>Whether to enable rule 18.10.4.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_5_1_enabled | <p>Whether to enable rule 18.10.5.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_6_1_enabled | <p>Whether to enable rule 18.10.6.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_6_2_enabled | <p>Whether to enable rule 18.10.6.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_6_2_force | <p>Whether to override the level requirement for CIS rule 18.10.6.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_8_1_enabled | <p>Whether to enable rule 18.10.8.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_8_2_enabled | <p>Whether to enable rule 18.10.8.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_8_3_enabled | <p>Whether to enable rule 18.10.8.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_9_1_1_enabled | <p>Whether to enable rule 18.10.9.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_1_1_enabled | <p>Whether to enable rule 18.10.10.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_1_1_force | <p>Whether to override the level requirement for CIS rule 18.10.10.1.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_10_1_2_enabled | <p>Whether to enable rule 18.10.10.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_1_2_force | <p>Whether to override the level requirement for CIS rule 18.10.10.1.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_10_1_3_enabled | <p>Whether to enable rule 18.10.10.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_1_3_force | <p>Whether to override the level requirement for CIS rule 18.10.10.1.3.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_10_1_4_enabled | <p>Whether to enable rule 18.10.10.1.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_1_4_force | <p>Whether to override the level requirement for CIS rule 18.10.10.1.4.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_10_1_5_enabled | <p>Whether to enable rule 18.10.10.1.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_1_5_force | <p>Whether to override the level requirement for CIS rule 18.10.10.1.5.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_10_1_6_enabled | <p>Whether to enable rule 18.10.10.1.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_1_6_force | <p>Whether to override the level requirement for CIS rule 18.10.10.1.6.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_10_1_7_enabled | <p>Whether to enable rule 18.10.10.1.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_1_7_force | <p>Whether to override the level requirement for CIS rule 18.10.10.1.7.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_10_1_8_enabled | <p>Whether to enable rule 18.10.10.1.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_1_8_force | <p>Whether to override the level requirement for CIS rule 18.10.10.1.8.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_10_1_9_enabled | <p>Whether to enable rule 18.10.10.1.9.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_1_9_force | <p>Whether to override the level requirement for CIS rule 18.10.10.1.9.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_10_1_10_enabled | <p>Whether to enable rule 18.10.10.1.10.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_1_10_force | <p>Whether to override the level requirement for CIS rule 18.10.10.1.10.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_fixed_drive_recovery_password | <p>Whether to allow or require a fixed drive 48-bit recovery password.</p> | str | no | <ul><li>allow</li><li>require</li></ul> | allow |
| w11cis_fixed_drive_recovery_key | <p>Whether to allow or require a fixed drive 256-bit recovery key.</p> | str | no | <ul><li>allow</li><li>require</li></ul> | allow |
| w11cis_rule_18_10_10_2_1_enabled | <p>Whether to enable rule 18.10.10.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_2_1_force | <p>Whether to override the level requirement for CIS rule 18.10.10.2.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_10_2_2_enabled | <p>Whether to enable rule 18.10.10.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_2_2_force | <p>Whether to override the level requirement for CIS rule 18.10.10.2.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_10_2_3_enabled | <p>Whether to enable rule 18.10.10.2.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_2_3_force | <p>Whether to override the level requirement for CIS rule 18.10.10.2.3.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_10_2_4_enabled | <p>Whether to enable rule 18.10.10.2.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_2_4_force | <p>Whether to override the level requirement for CIS rule 18.10.10.2.4.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_10_2_5_enabled | <p>Whether to enable rule 18.10.10.2.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_2_5_force | <p>Whether to override the level requirement for CIS rule 18.10.10.2.5.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_10_2_6_enabled | <p>Whether to enable rule 18.10.10.2.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_2_6_force | <p>Whether to override the level requirement for CIS rule 18.10.10.2.6.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_10_2_7_enabled | <p>Whether to enable rule 18.10.10.2.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_2_7_force | <p>Whether to override the level requirement for CIS rule 18.10.10.2.7.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_10_2_8_enabled | <p>Whether to enable rule 18.10.10.2.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_2_8_force | <p>Whether to override the level requirement for CIS rule 18.10.10.2.8.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_10_3_1_enabled | <p>Whether to enable rule 18.10.10.3.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_3_1_force | <p>Whether to override the level requirement for CIS rule 18.10.10.3.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_10_3_2_enabled | <p>Whether to enable rule 18.10.10.3.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_3_2_force | <p>Whether to override the level requirement for CIS rule 18.10.10.3.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_10_3_3_enabled | <p>Whether to enable rule 18.10.10.3.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_3_3_force | <p>Whether to override the level requirement for CIS rule 18.10.10.3.3.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_10_3_4_enabled | <p>Whether to enable rule 18.10.10.3.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_3_4_force | <p>Whether to override the level requirement for CIS rule 18.10.10.3.4.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_10_3_5_enabled | <p>Whether to enable rule 18.10.10.3.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_3_5_force | <p>Whether to override the level requirement for CIS rule 18.10.10.3.5.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_10_3_6_enabled | <p>Whether to enable rule 18.10.10.3.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_3_6_force | <p>Whether to override the level requirement for CIS rule 18.10.10.3.6.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_10_3_7_enabled | <p>Whether to enable rule 18.10.10.3.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_3_7_force | <p>Whether to override the level requirement for CIS rule 18.10.10.3.7.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_10_3_8_enabled | <p>Whether to enable rule 18.10.10.3.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_3_8_force | <p>Whether to override the level requirement for CIS rule 18.10.10.3.8.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_10_3_9_enabled | <p>Whether to enable rule 18.10.10.3.9.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_3_9_force | <p>Whether to override the level requirement for CIS rule 18.10.10.3.9.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_10_3_10_enabled | <p>Whether to enable rule 18.10.10.3.10.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_3_10_force | <p>Whether to override the level requirement for CIS rule 18.10.10.3.10.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_10_3_11_enabled | <p>Whether to enable rule 18.10.10.3.11.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_3_11_force | <p>Whether to override the level requirement for CIS rule 18.10.10.3.11.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_10_3_12_enabled | <p>Whether to enable rule 18.10.10.3.12.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_10_3_12_force | <p>Whether to override the level requirement for CIS rule 18.10.10.3.12.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_11_1_enabled | <p>Whether to enable rule 18.10.11.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_11_1_force | <p>Whether to override the level requirement for CIS rule 18.10.11.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_13_1_enabled | <p>Whether to enable rule 18.10.13.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_13_2_enabled | <p>Whether to enable rule 18.10.13.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_13_2_force | <p>Whether to override the level requirement for CIS rule 18.10.13.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_13_3_enabled | <p>Whether to enable rule 18.10.13.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_14_1_enabled | <p>Whether to enable rule 18.10.14.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_windows_connect_pin_requirement | <p>The Windows Connect PIN requirement.</p> | str | no | <ul><li>always</li><li>first_time</li></ul> | first_time |
| w11cis_rule_18_10_15_1_enabled | <p>Whether to enable rule 18.10.15.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_15_2_enabled | <p>Whether to enable rule 18.10.15.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_15_3_enabled | <p>Whether to enable rule 18.10.15.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_16_1_enabled | <p>Whether to enable rule 18.10.16.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_16_2_enabled | <p>Whether to enable rule 18.10.16.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_16_2_force | <p>Whether to override the level requirement for CIS rule 18.10.16.8.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_16_3_enabled | <p>Whether to enable rule 18.10.16.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_16_4_enabled | <p>Whether to enable rule 18.10.16.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_16_4_force | <p>Whether to override the level requirement for CIS rule 18.10.16.4.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_16_5_enabled | <p>Whether to enable rule 18.10.16.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_16_5_force | <p>Whether to override the level requirement for CIS rule 18.10.16.5.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_16_6_enabled | <p>Whether to enable rule 18.10.16.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_16_6_force | <p>Whether to override the level requirement for CIS rule 18.10.16.6.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_allow_telemetry | <p>Whether to allow telemetry.</p> | str | no | <ul><li>required</li><li>off</li></ul> | off |
| w11cis_rule_18_10_17_1_enabled | <p>Whether to enable rule 18.10.17.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_delivery_optimization_download_mode | <p>The Delivery Optimization download mode.</p><p>The `http_only` option does not allow peer-to-peer downloads.</p><p>The `lan` option allows peer-to-peer downloads from devices on the same local area network.</p><p>The `group` option allows peer-to-peer downloads from devices in the same group.</p><p>The `simple` option bypasses the Delivery Optimization cloud services for air-gapped environments.</p><p>The `bypass` option falls back to BITS instead of Delivery Optimization. This is not recommended because it is deprecated.</p> | str | no | <ul><li>http_only</li><li>lan</li><li>group</li><li>simple</li><li>bypass</li></ul> | lan |
| w11cis_rule_18_10_18_1_enabled | <p>Whether to enable rule 18.10.18.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_18_1_force | <p>Whether to override the level requirement for CIS rule 18.10.18.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_18_2_enabled | <p>Whether to enable rule 18.10.18.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_18_3_enabled | <p>Whether to enable rule 18.10.18.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_18_4_enabled | <p>Whether to enable rule 18.10.18.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_18_5_enabled | <p>Whether to enable rule 18.10.18.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_18_6_enabled | <p>Whether to enable rule 18.10.18.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_18_7_enabled | <p>Whether to enable rule 18.10.18.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_18_7_force | <p>Whether to override the level requirement for CIS rule 18.10.18.7.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_26_1_1_enabled | <p>Whether to enable rule 18.10.26.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_26_1_2_enabled | <p>Whether to enable rule 18.10.26.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_application_log_max_size_in_kb | <p>The maximum size of the Application log in KB.</p> | int | no |  | 32768 |
| w11cis_rule_18_10_26_2_1_enabled | <p>Whether to enable rule 18.10.26.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_26_2_2_enabled | <p>Whether to enable rule 18.10.26.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_security_log_max_size_in_kb | <p>The maximum size of the Security log in KB.</p> | int | no |  | 196608 |
| w11cis_rule_18_10_26_3_1_enabled | <p>Whether to enable rule 18.10.26.3.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_26_3_2_enabled | <p>Whether to enable rule 18.10.26.3.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_setup_log_max_size_in_kb | <p>The maximum size of the Setup log in KB.</p> | int | no |  | 32768 |
| w11cis_rule_18_10_26_4_1_enabled | <p>Whether to enable rule 18.10.26.4.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_26_4_2_enabled | <p>Whether to enable rule 18.10.26.4.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_system_log_max_size_in_kb | <p>The maximum size of the System log in KB.</p> | int | no |  | 32768 |
| w11cis_rule_18_10_29_2_enabled | <p>Whether to enable rule 18.10.29.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_29_2_force | <p>Whether to override the level requirement for CIS rule 18.10.29.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_29_3_enabled | <p>Whether to enable rule 18.10.29.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_29_4_enabled | <p>Whether to enable rule 18.10.29.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_29_5_enabled | <p>Whether to enable rule 18.10.29.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_29_6_enabled | <p>Whether to enable rule 18.10.29.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_36_1_enabled | <p>Whether to enable rule 18.10.36.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_36_1_force | <p>Whether to override the level requirement for CIS rule 18.10.36.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_40_1_enabled | <p>Whether to enable rule 18.10.40.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_40_1_force | <p>Whether to override the level requirement for CIS rule 18.10.40.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_41_1_enabled | <p>Whether to enable rule 18.10.41.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_43_1_enabled | <p>Whether to enable rule 18.10.43.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_43_2_enabled | <p>Whether to enable rule 18.10.43.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_43_3_enabled | <p>Whether to enable rule 18.10.43.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_43_4_enabled | <p>Whether to enable rule 18.10.43.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_43_5_enabled | <p>Whether to enable rule 18.10.43.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_43_6_enabled | <p>Whether to enable rule 18.10.43.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_49_1_enabled | <p>Whether to enable rule 18.10.49.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_49_1_force | <p>Whether to override the level requirement for CIS rule 18.10.49.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_50_1_enabled | <p>Whether to enable rule 18.10.50.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_50_1_force | <p>Whether to override the level requirement for CIS rule 18.10.50.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_56_1_enabled | <p>Whether to enable rule 18.10.56.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_56_1_force | <p>Whether to override the level requirement for CIS rule 18.10.56.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_57_2_2_enabled | <p>Whether to enable rule 18.10.57.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_57_2_2_force | <p>Whether to override the level requirement for CIS rule 18.10.57.2.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_57_2_3_enabled | <p>Whether to enable rule 18.10.57.2.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_57_3_2_1_enabled | <p>Whether to enable rule 18.10.57.3.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_57_3_2_1_force | <p>Whether to override the level requirement for CIS rule 18.10.57.3.2.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_57_3_3_1_enabled | <p>Whether to enable rule 18.10.57.3.3.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_57_3_3_1_force | <p>Whether to override the level requirement for CIS rule 18.10.57.3.3.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_57_3_3_2_enabled | <p>Whether to enable rule 18.10.57.3.3.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_57_3_3_2_force | <p>Whether to override the level requirement for CIS rule 18.10.57.3.3.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_57_3_3_3_enabled | <p>Whether to enable rule 18.10.57.3.3.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_57_3_3_4_enabled | <p>Whether to enable rule 18.10.57.3.3.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_57_3_3_4_force | <p>Whether to override the level requirement for CIS rule 18.10.57.3.3.4.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_57_3_3_5_enabled | <p>Whether to enable rule 18.10.57.3.3.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_57_3_3_5_force | <p>Whether to override the level requirement for CIS rule 18.10.57.3.3.5.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_57_3_3_6_enabled | <p>Whether to enable rule 18.10.57.3.3.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_57_3_3_6_force | <p>Whether to override the level requirement for CIS rule 18.10.57.3.3.6.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_57_3_3_7_enabled | <p>Whether to enable rule 18.10.57.3.3.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_57_3_3_7_force | <p>Whether to override the level requirement for CIS rule 18.10.57.3.3.7.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_57_3_3_8_enabled | <p>Whether to enable rule 18.10.57.3.3.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_57_3_3_8_force | <p>Whether to override the level requirement for CIS rule 18.10.57.3.3.8.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_57_3_9_1_enabled | <p>Whether to enable rule 18.10.57.3.9.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_57_3_9_2_enabled | <p>Whether to enable rule 18.10.57.3.9.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_57_3_9_3_enabled | <p>Whether to enable rule 18.10.57.3.9.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_57_3_9_4_enabled | <p>Whether to enable rule 18.10.57.3.9.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_57_3_9_5_enabled | <p>Whether to enable rule 18.10.57.3.9.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_57_3_10_1_enabled | <p>Whether to enable rule 18.10.57.3.10.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_57_3_10_1_force | <p>Whether to override the level requirement for CIS rule 18.10.57.3.10.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_remote_desktop_services_max_idle_time_in_ms | <p>The maximum idle time for Remote Desktop Services in milliseconds.</p> | int | no |  | 900000 |
| w11cis_rule_18_10_57_3_11_1_enabled | <p>Whether to enable rule 18.10.57.3.11.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_58_1_enabled | <p>Whether to enable rule 18.10.58.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_59_2_enabled | <p>Whether to enable rule 18.10.59.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_59_2_force | <p>Whether to override the level requirement for CIS rule 18.10.59.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_59_3_enabled | <p>Whether to enable rule 18.10.59.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_59_4_enabled | <p>Whether to enable rule 18.10.59.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_59_5_enabled | <p>Whether to enable rule 18.10.59.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_59_6_enabled | <p>Whether to enable rule 18.10.59.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_59_7_enabled | <p>Whether to enable rule 18.10.59.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_59_7_force | <p>Whether to override the level requirement for CIS rule 18.10.59.7.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_63_1_enabled | <p>Whether to enable rule 18.10.63.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_63_1_force | <p>Whether to override the level requirement for CIS rule 18.10.63.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_66_1_enabled | <p>Whether to enable rule 18.10.66.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_66_1_force | <p>Whether to override the level requirement for CIS rule 18.10.66.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_66_2_enabled | <p>Whether to enable rule 18.10.66.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_66_3_enabled | <p>Whether to enable rule 18.10.66.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_66_4_enabled | <p>Whether to enable rule 18.10.66.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_66_4_force | <p>Whether to override the level requirement for CIS rule 18.10.66.4.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_72_1_enabled | <p>Whether to enable rule 18.10.72.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_72_1_force | <p>Whether to override the level requirement for CIS rule 18.10.72.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_73_1_enabled | <p>Whether to enable rule 18.10.73.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_77_1_1_enabled | <p>Whether to enable rule 18.10.77.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_77_1_2_enabled | <p>Whether to enable rule 18.10.77.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_77_1_3_enabled | <p>Whether to enable rule 18.10.77.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_77_1_4_enabled | <p>Whether to enable rule 18.10.77.1.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_77_1_5_enabled | <p>Whether to enable rule 18.10.77.1.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_77_2_1_enabled | <p>Whether to enable rule 18.10.77.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_79_1_enabled | <p>Whether to enable rule 18.10.79.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_80_1_enabled | <p>Whether to enable rule 18.10.80.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_81_1_enabled | <p>Whether to enable rule 18.10.81.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_81_1_force | <p>Whether to override the level requirement for CIS rule 18.10.81.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_81_2_enabled | <p>Whether to enable rule 18.10.81.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_windows_ink_workspace_access | <p>The Windows Ink Workspace access.</p> | str | no | <ul><li>disallow_above_lock</li><li>disabled</li></ul> | disallow_above_lock |
| w11cis_rule_18_10_82_1_enabled | <p>Whether to enable rule 18.10.82.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_82_2_enabled | <p>Whether to enable rule 18.10.82.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_82_3_enabled | <p>Whether to enable rule 18.10.82.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_82_3_force | <p>Whether to override the level requirement for CIS rule 18.10.82.3.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_83_1_enabled | <p>Whether to enable rule 18.10.83.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_83_2_enabled | <p>Whether to enable rule 18.10.83.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_88_1_enabled | <p>Whether to enable rule 18.10.88.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_88_1_force | <p>Whether to override the level requirement for CIS rule 18.10.88.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_88_2_enabled | <p>Whether to enable rule 18.10.88.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_88_2_force | <p>Whether to override the level requirement for CIS rule 18.10.88.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_90_1_1_enabled | <p>Whether to enable rule 18.10.90.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_90_1_2_enabled | <p>Whether to enable rule 18.10.90.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_90_1_3_enabled | <p>Whether to enable rule 18.10.90.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_90_2_1_enabled | <p>Whether to enable rule 18.10.90.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_90_2_2_enabled | <p>Whether to enable rule 18.10.90.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_90_2_2_force | <p>Whether to override the level requirement for CIS rule 18.10.90.2.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_90_2_3_enabled | <p>Whether to enable rule 18.10.90.2.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_90_2_4_enabled | <p>Whether to enable rule 18.10.90.2.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_91_1_enabled | <p>Whether to enable rule 18.10.91.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_91_1_force | <p>Whether to override the level requirement for CIS rule 18.10.91.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_92_1_enabled | <p>Whether to enable rule 18.10.92.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_92_2_enabled | <p>Whether to enable rule 18.10.92.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_92_2_force | <p>Whether to override the level requirement for CIS rule 18.10.92.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_18_10_92_3_enabled | <p>Whether to enable rule 18.10.92.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_93_2_1_enabled | <p>Whether to enable rule 18.10.93.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_94_1_1_enabled | <p>Whether to enable rule 18.10.94.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_94_2_1_enabled | <p>Whether to enable rule 18.10.94.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_94_2_2_enabled | <p>Whether to enable rule 18.10.94.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_94_2_3_enabled | <p>Whether to enable rule 18.10.94.2.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_94_2_4_enabled | <p>Whether to enable rule 18.10.94.2.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_94_4_1_enabled | <p>Whether to enable rule 18.10.94.4.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_94_4_2_enabled | <p>Whether to enable rule 18.10.94.4.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_10_94_4_3_enabled | <p>Whether to enable rule 18.10.94.4.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_11_1_enabled | <p>Whether to enable rule 18.11.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_18_11_2_enabled | <p>Whether to enable rule 18.11.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_disable_http_proxy_features | <p>The HTTP proxy features to disable.</p> | str | no | <ul><li>disable_for_loopback_interfaces</li><li>disable_all</li></ul> | disable_for_loopback_interfaces |
| w11cis_rule_19_5_1_1_enabled | <p>Whether to enable rule 19.5.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_19_6_6_1_1_enabled | <p>Whether to enable rule 19.6.6.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_19_6_6_1_1_force | <p>Whether to override the level requirement for CIS rule 19.6.6.1.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_19_7_5_1_enabled | <p>Whether to enable rule 19.7.5.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_19_7_5_2_enabled | <p>Whether to enable rule 19.7.5.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_19_7_8_1_enabled | <p>Whether to enable rule 19.7.8.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_19_7_8_2_enabled | <p>Whether to enable rule 19.7.8.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_19_7_8_3_enabled | <p>Whether to enable rule 19.7.8.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_19_7_8_3_force | <p>Whether to override the level requirement for CIS rule 19.7.8.3.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_19_7_8_4_enabled | <p>Whether to enable rule 19.7.8.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_19_7_8_4_force | <p>Whether to override the level requirement for CIS rule 19.7.8.4.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| w11cis_rule_19_7_8_5_enabled | <p>Whether to enable rule 19.7.8.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_19_7_26_1_enabled | <p>Whether to enable rule 19.7.26.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_19_7_46_2_1_enabled | <p>Whether to enable rule 19.7.46.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| w11cis_rule_19_7_46_2_1_force | <p>Whether to override the level requirement for CIS rule 19.7.46.2.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |


## License
MIT

## Author and Project Information
Jim Tarpley (@trippsc2)
<!-- END_ANSIBLE_DOCS -->
