<!-- BEGIN_ANSIBLE_DOCS -->

# Ansible Role: trippsc2.cis.rhel8
Version: 1.4.1

This role applies the CIS Benchmark hardening steps on RHEL8-based machines.  It is based on the CIS Benchmark for RHEL 8, v3.0.0.

## Requirements

| Platform | Versions |
| -------- | -------- |
| EL | <ul><li>8</li></ul> |

## Dependencies

| Collection |
| ---------- |
| ansible.posix |
| community.general |

## Role Arguments
|Option|Description|Type|Required|Choices|Default|
|---|---|---|---|---|---|
| rhel8cis_skip_reboot | <p>Whether to skip the reboot step.</p> | bool | no |  | True |
| rhel8cis_level | <p>The CIS benchmark level to apply.</p> | int | no | <ul><li>1</li><li>2</li></ul> | 2 |
| rhel8cis_machine_type | <p>The type of machine for which to apply the CIS benchmarks.</p> | str | no | <ul><li>server</li><li>workstation</li></ul> | server |
| rhel8cis_rule_1_1_1_1_enabled | <p>Whether to apply CIS rule 1.1.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_1_2_enabled | <p>Whether to apply CIS rule 1.1.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_1_3_enabled | <p>Whether to apply CIS rule 1.1.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_1_4_enabled | <p>Whether to apply CIS rule 1.1.1.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_1_5_enabled | <p>Whether to apply CIS rule 1.1.1.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_1_6_enabled | <p>Whether to apply CIS rule 1.1.1.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_1_6_force | <p>Whether to override the level requirement for CIS rule 1.1.1.6.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_1_1_1_7_enabled | <p>Whether to apply CIS rule 1.1.1.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_1_7_force | <p>Whether to override the level requirement for CIS rule 1.1.1.7.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_1_1_1_8_enabled | <p>Whether to apply CIS rule 1.1.1.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_1_8_force | <p>Whether to override the level requirement for CIS rule 1.1.1.8.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_1_1_1_9_enabled | <p>Whether to apply CIS rule 1.1.1.9.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_1_10_enabled | <p>Whether to apply CIS rule 1.1.1.10.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_1_10_force | <p>Whether to override the level requirement for CIS rule 1.1.1.10.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_1_1_1_11_enabled | <p>Whether to apply CIS rule 1.1.1.11.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_ceph_needed | <p>Whether the Ceph filesystem is needed.</p><p>If set to `false` and the rule to disable unneeded filesystems is enabled, the Ceph filesystem kernel module will be disabled.</p> | bool | no |  | True |
| rhel8cis_cifs_needed | <p>Whether the CIFS filesystem is needed.</p><p>If set to `false` and the rule to disable unneeded filesystems is enabled, the CIFS filesystem kernel module will be disabled.</p> | bool | no |  | True |
| rhel8cis_exfat_needed | <p>Whether the exFAT filesystem is needed.</p><p>If set to `false` and the rule to disable unneeded filesystems is enabled, the exFAT filesystem kernel module will be disabled.</p> | bool | no |  | True |
| rhel8cis_ext_needed | <p>Whether the ext filesystem is needed.</p><p>If set to `false` and the rule to disable unneeded filesystems is enabled, the ext filesystem kernel module will be disabled.</p> | bool | no |  | True |
| rhel8cis_fat_needed | <p>Whether the FAT filesystem is needed.</p><p>If set to `false` and the rule to disable unneeded filesystems is enabled, the FAT filesystem kernel module will be disabled.</p> | bool | no |  | True |
| rhel8cis_fscache_needed | <p>Whether the fscache filesystem is needed.</p><p>If set to `false` and the rule to disable unneeded filesystems is enabled, the fscache filesystem kernel module will be disabled.</p> | bool | no |  | True |
| rhel8cis_fuse_needed | <p>Whether the FUSE filesystem is needed.</p><p>If set to `false` and the rule to disable unneeded filesystems is enabled, the FUSE filesystem kernel module will be disabled.</p> | bool | no |  | True |
| rhel8cis_gfs2_needed | <p>Whether the GFS2 filesystem is needed.</p><p>If set to `false` and the rule to disable unneeded filesystems is enabled, the GFS2 filesystem kernel module will be disabled.</p> | bool | no |  | True |
| rhel8cis_nfs_common_needed | <p>Whether the NFS common filesystem is needed.</p><p>If set to `false` and the rule to disable unneeded filesystems is enabled, the NFS common filesystem kernel module will be disabled.</p> | bool | no |  | True |
| rhel8cis_nfsd_needed | <p>Whether the NFSd filesystem is needed.</p><p>If set to `false` and the rule to disable unneeded filesystems is enabled, the NFSd filesystem kernel module will be disabled.</p> | bool | no |  | True |
| rhel8cis_smbfs_common_needed | <p>Whether the SMBFS common filesystem is needed.</p><p>If set to `false` and the rule to disable unneeded filesystems is enabled, the SMBFS common filesystem kernel module will be disabled.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_2_1_1_enabled | <p>Whether to apply CIS rule 1.1.2.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_2_1_2_enabled | <p>Whether to apply CIS rule 1.1.2.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_2_1_3_enabled | <p>Whether to apply CIS rule 1.1.2.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_2_1_4_enabled | <p>Whether to apply CIS rule 1.1.2.1.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_tmp_mount_opts | <p>The mount options for the /tmp partition.</p> | list of 'str' | no |  | ['defaults', 'nodev', 'nosuid', 'noexec'] |
| rhel8cis_rule_1_1_2_2_1_enabled | <p>Whether to apply CIS rule 1.1.2.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_2_2_2_enabled | <p>Whether to apply CIS rule 1.1.2.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_2_2_3_enabled | <p>Whether to apply CIS rule 1.1.2.2.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_2_2_4_enabled | <p>Whether to apply CIS rule 1.1.2.2.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_dev_shm_mount_opts | <p>The mount options for the /dev/shm partition.</p> | list of 'str' | no |  | ['mode=1777', 'strictatime', 'nodev', 'nosuid', 'noexec'] |
| rhel8cis_rule_1_1_2_3_1_enabled | <p>Whether to apply CIS rule 1.1.2.3.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_2_3_1_force | <p>Whether to override the level requirement for CIS rule 1.1.2.3.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_1_1_2_3_2_enabled | <p>Whether to apply CIS rule 1.1.2.3.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_2_3_3_enabled | <p>Whether to apply CIS rule 1.1.2.3.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_home_mount_with_uuid | <p>Whether to use UUIDs instead device path for /home in /etc/fstab.</p> | bool | no |  | True |
| rhel8cis_home_mount_opts | <p>The mount options for the /home partition.</p> | list of 'str' | no |  | ['defaults', 'nodev', 'nosuid'] |
| rhel8cis_rule_1_1_2_4_1_enabled | <p>Whether to apply CIS rule 1.1.2.4.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_2_4_1_force | <p>Whether to override the level requirement for CIS rule 1.1.2.4.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_1_1_2_4_2_enabled | <p>Whether to apply CIS rule 1.1.2.4.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_2_4_3_enabled | <p>Whether to apply CIS rule 1.1.2.4.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_var_mount_with_uuid | <p>Whether to use UUIDs instead device path for /var in /etc/fstab.</p> | bool | no |  | True |
| rhel8cis_var_mount_opts | <p>The mount options for the /var partition.</p> | list of 'str' | no |  | ['defaults', 'nodev', 'nosuid'] |
| rhel8cis_rule_1_1_2_5_1_enabled | <p>Whether to apply CIS rule 1.1.2.5.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_2_5_1_force | <p>Whether to override the level requirement for CIS rule 1.1.2.5.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_1_1_2_5_2_enabled | <p>Whether to apply CIS rule 1.1.2.5.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_2_5_3_enabled | <p>Whether to apply CIS rule 1.1.2.5.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_2_5_4_enabled | <p>Whether to apply CIS rule 1.1.2.5.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_var_tmp_mount_with_uuid | <p>Whether to use UUIDs instead device path for /var/tmp in /etc/fstab.</p> | bool | no |  | True |
| rhel8cis_var_tmp_mount_opts | <p>The mount options for the /var/tmp partition.</p> | list of 'str' | no |  | ['defaults', 'nodev', 'nosuid', 'noexec'] |
| rhel8cis_rule_1_1_2_6_1_enabled | <p>Whether to apply CIS rule 1.1.2.6.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_2_6_1_force | <p>Whether to override the level requirement for CIS rule 1.1.2.6.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_1_1_2_6_2_enabled | <p>Whether to apply CIS rule 1.1.2.6.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_2_6_3_enabled | <p>Whether to apply CIS rule 1.1.2.6.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_2_6_4_enabled | <p>Whether to apply CIS rule 1.1.2.6.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_var_log_mount_with_uuid | <p>Whether to use UUIDs instead device path for /var/log in /etc/fstab.</p> | bool | no |  | True |
| rhel8cis_var_log_mount_opts | <p>The mount options for the /var/log partition.</p> | list of 'str' | no |  | ['defaults', 'nodev', 'nosuid', 'noexec'] |
| rhel8cis_rule_1_1_2_7_1_enabled | <p>Whether to apply CIS rule 1.1.2.7.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_2_7_1_force | <p>Whether to override the level requirement for CIS rule 1.1.2.7.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_1_1_2_7_2_enabled | <p>Whether to apply CIS rule 1.1.2.7.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_2_7_3_enabled | <p>Whether to apply CIS rule 1.1.2.7.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_1_2_7_4_enabled | <p>Whether to apply CIS rule 1.1.2.7.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_var_log_audit_mount_with_uuid | <p>Whether to use UUIDs instead device path for /var/log/audit in /etc/fstab.</p> | bool | no |  | True |
| rhel8cis_var_log_audit_mount_opts | <p>The mount options for the /var/log/audit partition.</p> | list of 'str' | no |  | ['defaults', 'nodev', 'nosuid', 'noexec'] |
| rhel8cis_rule_1_2_1_1_enabled | <p>Whether to apply CIS rule 1.2.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_2_1_2_enabled | <p>Whether to apply CIS rule 1.2.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_2_1_3_enabled | <p>Whether to apply CIS rule 1.2.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_2_1_3_force | <p>Whether to override the level requirement for CIS rule 1.2.1.3.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_1_2_1_4_enabled | <p>Whether to apply CIS rule 1.2.1.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_2_1_5_enabled | <p>Whether to apply CIS rule 1.2.1.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_2_1_5_force | <p>Whether to override the level requirement for CIS rule 1.2.1.5.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_1_2_2_1_enabled | <p>Whether to apply CIS rule 1.2.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_3_1_1_enabled | <p>Whether to apply CIS rule 1.3.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_3_1_2_enabled | <p>Whether to apply CIS rule 1.3.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_3_1_3_enabled | <p>Whether to apply CIS rule 1.3.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_3_1_4_enabled | <p>Whether to apply CIS rule 1.3.1.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_3_1_5_enabled | <p>Whether to apply CIS rule 1.3.1.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_3_1_5_force | <p>Whether to override the level requirement for CIS rule 1.3.1.5.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_1_3_1_6_enabled | <p>Whether to apply CIS rule 1.3.1.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_3_1_6_force | <p>Whether to override the level requirement for CIS rule 1.3.1.6.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_1_3_1_7_enabled | <p>Whether to apply CIS rule 1.3.1.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_3_1_8_enabled | <p>Whether to apply CIS rule 1.3.1.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_selinux_policy | <p>The SELinux policy to use.</p> | str | no | <ul><li>targeted</li><li>mls</li></ul> | targeted |
| rhel8cis_selinux_mode | <p>The SELinux mode to use.</p> | str | no | <ul><li>enforcing</li><li>permissive</li></ul> | enforcing |
| rhel8cis_rule_1_4_1_enabled | <p>Whether to apply CIS rule 1.4.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_4_2_enabled | <p>Whether to apply CIS rule 1.4.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_force_reset_bootloader_password | <p>Whether to force a reset of the bootloader password, even if one is set.</p><p>If set to `true`, the bootloader password will be reset to the value of *rhel8cis_bootloader_password* always, making the role not idempotent.</p><p>If set to `false`, the bootloader password will only be set if it is not already set.</p> | bool | no |  | False |
| rhel8cis_bootloader_password | <p>The bootloader password to set.</p><p>If the rule requiring a bootloader password is enabled, this is required.</p> | str | no |  |  |
| rhel8cis_rule_1_5_1_enabled | <p>Whether to apply CIS rule 1.5.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_5_2_enabled | <p>Whether to apply CIS rule 1.5.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_5_3_enabled | <p>Whether to apply CIS rule 1.5.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_5_3_force | <p>Whether to override the level requirement for CIS rule 1.5.3.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_1_5_4_enabled | <p>Whether to apply CIS rule 1.5.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_5_5_enabled | <p>Whether to apply CIS rule 1.5.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_5_6_enabled | <p>Whether to apply CIS rule 1.5.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_kptr_restrict | <p>The kptr restrict level to configure.</p> | str | no | <ul><li>mask_unprivileged</li><li>mask_all</li></ul> | mask_unprivileged |
| rhel8cis_rule_1_5_7_enabled | <p>Whether to apply CIS rule 1.5.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_ptrace_scope | <p>The ptrace scope to configure.</p> | str | no | <ul><li>restricted_ptrace</li><li>admin_only_attach</li><li>no_attach</li></ul> | restricted_ptrace |
| rhel8cis_rule_1_5_8_enabled | <p>Whether to apply CIS rule 1.5.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_5_9_enabled | <p>Whether to apply CIS rule 1.5.9.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_5_10_enabled | <p>Whether to apply CIS rule 1.5.10.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_6_1_enabled | <p>Whether to apply CIS rule 1.6.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_6_2_enabled | <p>Whether to apply CIS rule 1.6.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_6_3_enabled | <p>Whether to apply CIS rule 1.6.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_6_4_enabled | <p>Whether to apply CIS rule 1.6.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_6_5_enabled | <p>Whether to apply CIS rule 1.6.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_6_6_enabled | <p>Whether to apply CIS rule 1.6.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_crypto_policy | <p>The crypto policy to configure.</p><p>Setting this to `LEGACY` will cause the role to fail validation if the rule forbidding it is enabled.</p><p>Setting this to `FIPS` will **not** cause the server to be converted to FIPS mode.</p> | str | no | <ul><li>DEFAULT</li><li>FUTURE</li><li>FIPS</li><li>LEGACY</li></ul> | DEFAULT |
| rhel8cis_additional_crypto_subpolicies | <p>The additional crypto subpolicies to configure.</p><p>This should not include the subpolicies needed to comply with benchmark rules.</p> | list of 'str' | no |  | [] |
| rhel8cis_rule_1_7_1_enabled | <p>Whether to apply CIS rule 1.7.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_7_2_enabled | <p>Whether to apply CIS rule 1.7.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_7_3_enabled | <p>Whether to apply CIS rule 1.7.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_7_4_enabled | <p>Whether to apply CIS rule 1.7.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_7_5_enabled | <p>Whether to apply CIS rule 1.7.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_7_6_enabled | <p>Whether to apply CIS rule 1.7.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_use_motd | <p>Whether to use the Message of the Day (MOTD) banner.</p><p>This banner appears for all local and remote logins.</p><p>If this is set to `false`, the banner contents will be removed.</p> | bool | no |  | True |
| rhel8cis_motd_banner | <p>The banner contents to use for the Message of the Day (MOTD).</p><p>If *rhel8cis_use_motd* is set to `false`, this will be ignored and the MOTD banner contents will be removed.</p> | str | no |  | Authorized users only.\n\nAll activity may be monitored and reported.\n\n |
| rhel8cis_use_issue | <p>Whether to use the local login warning banner.</p><p>This banner appears only for local logins, in additional to the Message of the Day (MOTD) banner.</p><p>If this is set to `false`, the banner contents will be removed.</p> | bool | no |  | False |
| rhel8cis_issue_banner | <p>The banner contents to use for the local login warning banner.</p><p>If *rhel8cis_use_issue* is set to `false`, this will be ignored and the local login warning banner contents will be removed.</p> | str | no |  | Authorized users only.\n\nAll activity may be monitored and reported.\n\n |
| rhel8cis_use_issue_net | <p>Whether to use the remote login warning banner.</p><p>This banner appears only for remote logins, in additional to the Message of the Day (MOTD) banner.</p><p>If this is set to `false`, the banner contents will be removed.</p> | bool | no |  | False |
| rhel8cis_issue_net_banner | <p>The banner contents to use for the remote login warning banner.</p><p>If *rhel8cis_use_issue_net* is set to `false`, this will be ignored and the remote login warning banner contents will be removed.</p> | str | no |  | Authorized users only.\n\nAll activity may be monitored and reported.\n\n |
| rhel8cis_rule_1_8_1_enabled | <p>Whether to apply CIS rule 1.8.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_8_2_enabled | <p>Whether to apply CIS rule 1.8.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_8_3_enabled | <p>Whether to apply CIS rule 1.8.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_8_4_enabled | <p>Whether to apply CIS rule 1.8.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_8_4_force | <p>Whether to override the level requirement for CIS rule 1.8.4.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_1_8_5_enabled | <p>Whether to apply CIS rule 1.8.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_8_6_enabled | <p>Whether to apply CIS rule 1.8.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_8_7_enabled | <p>Whether to apply CIS rule 1.8.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_1_8_7_force | <p>Whether to override the level requirement for CIS rule 1.8.7.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_2_1_1_enabled | <p>Whether to apply CIS rule 2.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_1_1_force | <p>Whether to override the level requirement for CIS rule 2.1.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_2_1_2_enabled | <p>Whether to apply CIS rule 2.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_1_2_force | <p>Whether to override the level requirement for CIS rule 2.1.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_2_1_3_enabled | <p>Whether to apply CIS rule 2.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_1_3_force | <p>Whether to override the level requirement for CIS rule 2.1.3.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_2_1_4_enabled | <p>Whether to apply CIS rule 2.1.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_1_5_enabled | <p>Whether to apply CIS rule 2.1.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_1_6_enabled | <p>Whether to apply CIS rule 2.1.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_1_7_enabled | <p>Whether to apply CIS rule 2.1.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_1_8_enabled | <p>Whether to apply CIS rule 2.1.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_1_9_enabled | <p>Whether to apply CIS rule 2.1.9.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_1_10_enabled | <p>Whether to apply CIS rule 2.1.10.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_1_11_enabled | <p>Whether to apply CIS rule 2.1.11.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_1_12_enabled | <p>Whether to apply CIS rule 2.1.12.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_1_13_enabled | <p>Whether to apply CIS rule 2.1.13.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_1_14_enabled | <p>Whether to apply CIS rule 2.1.14.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_1_15_enabled | <p>Whether to apply CIS rule 2.1.15.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_1_16_enabled | <p>Whether to apply CIS rule 2.1.16.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_1_17_enabled | <p>Whether to apply CIS rule 2.1.17.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_1_18_enabled | <p>Whether to apply CIS rule 2.1.18.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_1_19_enabled | <p>Whether to apply CIS rule 2.1.19.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_1_20_enabled | <p>Whether to apply CIS rule 2.1.20.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_1_21_enabled | <p>Whether to apply CIS rule 2.1.21.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_1_21_force | <p>Whether to override the level requirement for CIS rule 2.1.21.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_2_1_22_enabled | <p>Whether to apply CIS rule 2.1.22.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_1_22_force | <p>Whether to override the level requirement for CIS rule 2.1.22.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_2_1_23_enabled | <p>Whether to apply CIS rule 2.1.23.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_1_24_enabled | <p>Whether to apply CIS rule 2.1.24.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_autofs_package_needed | <p>Whether the `autofs` package is needed.</p><p>If set to `true`, the `autofs` package will be remain installed and the services will be disabled instead.</p> | bool | no |  | False |
| rhel8cis_avahi_package_needed | <p>Whether the `avahi` package is needed.</p><p>If set to `true`, the `avahi` package will be remain installed and the services will be disabled instead.</p> | bool | no |  | False |
| rhel8cis_cockpit_ws_needed | <p>Whether the `cockpit-ws` package is needed.</p><p>If set to `true`, the `cockpit-ws` package will be remain installed and the services will be disabled instead.</p> | bool | no |  | False |
| rhel8cis_dhcp_server_package_needed | <p>Whether the `dhcp-server` package is needed.</p><p>If set to `true`, the `dhcp-server` package will be remain installed and the services will be disabled instead.</p> | bool | no |  | False |
| rhel8cis_bind_package_needed | <p>Whether the `bind` package is needed.</p><p>If set to `true`, the `bind` package will be remain installed and the services will be disabled instead.</p> | bool | no |  | False |
| rhel8cis_dnsmasq_package_needed | <p>Whether the `dnsmasq` package is needed.</p><p>If set to `true`, the `dnsmasq` package will be remain installed and the services will be disabled instead.</p> | bool | no |  | False |
| rhel8cis_samba_package_needed | <p>Whether the `samba` package is needed.</p><p>If set to `true`, the `samba` package will be remain installed and the services will be disabled instead.</p> | bool | no |  | False |
| rhel8cis_vsftpd_package_needed | <p>Whether the `vsftpd` package is needed.</p><p>If set to `true`, the `vsftpd` package will be remain installed and the services will be disabled instead.</p> | bool | no |  | False |
| rhel8cis_dovecot_package_needed | <p>Whether the `dovecot` package is needed.</p><p>If set to `true`, the `dovecot` package will be remain installed and the services will be disabled instead.</p> | bool | no |  | False |
| rhel8cis_cyrus_imapd_package_needed | <p>Whether the `cyrus-imapd` package is needed.</p><p>If set to `true`, the `cyrus-imapd` package will be remain installed and the services will be disabled instead.</p> | bool | no |  | False |
| rhel8cis_nfs_utils_package_needed | <p>Whether the `nfs-utils` package is needed.</p><p>If set to `true`, the `nfs-utils` package will be remain installed and the services will be disabled instead.</p> | bool | no |  | False |
| rhel8cis_ypserv_package_needed | <p>Whether the `ypserv` package is needed.</p><p>If set to `true`, the `ypserv` package will be remain installed and the services will be disabled instead.</p> | bool | no |  | False |
| rhel8cis_cups_package_needed | <p>Whether the `cups` package is needed.</p><p>If set to `true`, the `cups` package will be remain installed and the services will be disabled instead.</p> | bool | no |  | False |
| rhel8cis_rpcbind_package_needed | <p>Whether the `rpcbind` package is needed.</p><p>If set to `true`, the `rpcbind` package will be remain installed and the services will be disabled instead.</p> | bool | no |  | False |
| rhel8cis_rsync_daemon_package_needed | <p>Whether the `rsync-daemon` package is needed.</p><p>If set to `true`, the `rsync-daemon` package will be remain installed and the services will be disabled instead.</p> | bool | no |  | False |
| rhel8cis_net_snmp_package_needed | <p>Whether the `net-snmp` package is needed.</p><p>If set to `true`, the `net-snmp` package will be remain installed and the services will be disabled instead.</p> | bool | no |  | False |
| rhel8cis_telnet_server_package_needed | <p>Whether the `telnet-server` package is needed.</p><p>If set to `true`, the `telnet-server` package will be remain installed and the services will be disabled instead.</p> | bool | no |  | False |
| rhel8cis_tftp_server_package_needed | <p>Whether the `tftp-server` package is needed.</p><p>If set to `true`, the `tftp-server` package will be remain installed and the services will be disabled instead.</p> | bool | no |  | False |
| rhel8cis_squid_package_needed | <p>Whether the `squid` package is needed.</p><p>If set to `true`, the `squid` package will be remain installed and the services will be disabled instead.</p> | bool | no |  | False |
| rhel8cis_httpd_needed | <p>Whether the `httpd` package is needed.</p><p>If set to `true`, the `httpd` package will be remain installed.</p> | bool | no |  | False |
| rhel8cis_nginx_needed | <p>Whether the `nginx` package is needed.</p><p>If set to `true`, the `nginx` package will be remain installed.</p> | bool | no |  | False |
| rhel8cis_xinetd_package_needed | <p>Whether the `xinetd` package is needed.</p><p>If set to `true`, the `xinetd` package will be remain installed and the services will be disabled instead.</p> | bool | no |  | False |
| rhel8cis_xorg_needed | <p>Whether the `xorg` package is needed.</p><p>If set to `true`, the `xorg` package will be remain installed and the services will be disabled instead.</p> | bool | no |  | False |
| rhel8cis_rule_2_2_1_enabled | <p>Whether to apply CIS rule 2.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_2_2_enabled | <p>Whether to apply CIS rule 2.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_2_2_force | <p>Whether to override the level requirement for CIS rule 2.2.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_2_2_3_enabled | <p>Whether to apply CIS rule 2.2.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_2_4_enabled | <p>Whether to apply CIS rule 2.2.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_2_5_enabled | <p>Whether to apply CIS rule 2.2.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_3_1_enabled | <p>Whether to apply CIS rule 2.3.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_3_2_enabled | <p>Whether to apply CIS rule 2.3.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_3_3_enabled | <p>Whether to apply CIS rule 2.3.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_chrony_servers | <p>The NTP server configuration to use with chrony.</p> | list of dicts of 'rhel8cis_chrony_servers' options | no |  | [{'name': '0.pool.ntp.org', 'options': ['minpoll 8']}, {'name': '1.pool.ntp.org', 'options': ['minpoll 8']}, {'name': '2.pool.ntp.org', 'options': ['minpoll 8']}, {'name': '3.pool.ntp.org', 'options': ['minpoll 8']}] |
| rhel8cis_rule_2_4_1_1_enabled | <p>Whether to apply CIS rule 2.4.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_4_1_2_enabled | <p>Whether to apply CIS rule 2.4.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_4_1_3_enabled | <p>Whether to apply CIS rule 2.4.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_4_1_4_enabled | <p>Whether to apply CIS rule 2.4.1.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_4_1_5_enabled | <p>Whether to apply CIS rule 2.4.1.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_4_1_6_enabled | <p>Whether to apply CIS rule 2.4.1.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_4_1_7_enabled | <p>Whether to apply CIS rule 2.4.1.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_4_1_8_enabled | <p>Whether to apply CIS rule 2.4.1.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_4_1_9_enabled | <p>Whether to apply CIS rule 2.4.1.9.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_2_4_2_1_enabled | <p>Whether to apply CIS rule 2.4.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_1_1_enabled | <p>Whether to apply CIS rule 3.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_1_2_enabled | <p>Whether to apply CIS rule 3.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_1_3_enabled | <p>Whether to apply CIS rule 3.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_1_3_force | <p>Whether to override the level requirement for CIS rule 3.1.3.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_ipv6_needed | <p>Whether IPv6 is needed.</p> | bool | no |  | False |
| rhel8cis_bluez_package_needed | <p>Whether the `bluez` package is needed.</p><p>If set to `true`, the `bluez` package will be remain installed and the services will be disabled instead.</p><p>If *rhel8cis_machine_type* is set to `workstation` or *rhel8cis_xorg_needed* is set to `true`, this will default to `true`.  Otherwise, it will default to `false`.</p> | bool | no |  |  |
| rhel8cis_rule_3_2_1_enabled | <p>Whether to apply CIS rule 3.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_2_2_enabled | <p>Whether to apply CIS rule 3.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_2_3_enabled | <p>Whether to apply CIS rule 3.2.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_2_4_enabled | <p>Whether to apply CIS rule 3.2.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_2_5_enabled | <p>Whether to apply CIS rule 3.2.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_2_5_force | <p>Whether to override the level requirement for CIS rule 3.2.5.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_3_2_6_enabled | <p>Whether to apply CIS rule 3.2.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_3_1_1_enabled | <p>Whether to apply CIS rule 3.3.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_3_1_1_force | <p>Whether to override the level requirement for CIS rule 3.3.1.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_3_3_1_2_enabled | <p>Whether to apply CIS rule 3.3.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_3_1_3_enabled | <p>Whether to apply CIS rule 3.3.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_3_1_4_enabled | <p>Whether to apply CIS rule 3.3.1.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_3_1_5_enabled | <p>Whether to apply CIS rule 3.3.1.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_3_1_6_enabled | <p>Whether to apply CIS rule 3.3.1.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_3_1_7_enabled | <p>Whether to apply CIS rule 3.3.1.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_3_1_8_enabled | <p>Whether to apply CIS rule 3.3.1.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_3_1_9_enabled | <p>Whether to apply CIS rule 3.3.1.9.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_3_1_10_enabled | <p>Whether to apply CIS rule 3.3.1.10.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_3_1_11_enabled | <p>Whether to apply CIS rule 3.3.1.11.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_3_1_12_enabled | <p>Whether to apply CIS rule 3.3.1.12.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_3_1_13_enabled | <p>Whether to apply CIS rule 3.3.1.13.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_3_1_14_enabled | <p>Whether to apply CIS rule 3.3.1.14.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_3_1_15_enabled | <p>Whether to apply CIS rule 3.3.1.15.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_3_1_16_enabled | <p>Whether to apply CIS rule 3.3.1.16.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_3_1_17_enabled | <p>Whether to apply CIS rule 3.3.1.17.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_3_1_18_enabled | <p>Whether to apply CIS rule 3.3.1.18.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_3_2_1_enabled | <p>Whether to apply CIS rule 3.3.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_3_2_2_enabled | <p>Whether to apply CIS rule 3.3.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_3_2_3_enabled | <p>Whether to apply CIS rule 3.3.2.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_3_2_4_enabled | <p>Whether to apply CIS rule 3.3.2.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_3_2_5_enabled | <p>Whether to apply CIS rule 3.3.2.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_3_2_6_enabled | <p>Whether to apply CIS rule 3.3.2.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_3_2_7_enabled | <p>Whether to apply CIS rule 3.3.2.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_3_3_2_8_enabled | <p>Whether to apply CIS rule 3.3.2.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_4_1_1_enabled | <p>Whether to apply CIS rule 4.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_4_1_2_enabled | <p>Whether to apply CIS rule 4.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_firewalld_backend | <p>The firewall backend to use.</p> | str | no | <ul><li>nftables</li><li>iptables</li></ul> | nftables |
| rhel8cis_rule_4_1_3_enabled | <p>Whether to apply CIS rule 4.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_4_1_4_enabled | <p>Whether to apply CIS rule 4.1.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_firewalld_active_zone | <p>The name of the firewalld active zone to use.</p> | str | no |  | public |
| rhel8cis_firewalld_active_zone_target | <p>The target of the firewalld active zone to use for non-matching incoming traffic.</p> | str | no | <ul><li>DROP</li><li>%%REJECT%%</li></ul> | DROP |
| rhel8cis_rule_4_1_5_enabled | <p>Whether to apply CIS rule 4.1.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_4_1_6_enabled | <p>Whether to apply CIS rule 4.1.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_4_1_7_enabled | <p>Whether to apply CIS rule 4.1.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_1_1_enabled | <p>Whether to apply CIS rule 5.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_1_2_enabled | <p>Whether to apply CIS rule 5.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_1_3_enabled | <p>Whether to apply CIS rule 5.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_1_4_enabled | <p>Whether to apply CIS rule 5.1.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_1_5_enabled | <p>Whether to apply CIS rule 5.1.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_1_6_enabled | <p>Whether to apply CIS rule 5.1.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_1_7_enabled | <p>Whether to apply CIS rule 5.1.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_1_8_enabled | <p>Whether to apply CIS rule 5.1.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_1_9_enabled | <p>Whether to apply CIS rule 5.1.9.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_1_10_enabled | <p>Whether to apply CIS rule 5.1.10.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_1_10_force | <p>Whether to override the level requirement for CIS rule 5.1.10.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_5_1_11_enabled | <p>Whether to apply CIS rule 5.1.11.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_1_11_force | <p>Whether to override the level requirement for CIS rule 5.1.11.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_5_1_12_enabled | <p>Whether to apply CIS rule 5.1.12.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_1_13_enabled | <p>Whether to apply CIS rule 5.1.13.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_1_14_enabled | <p>Whether to apply CIS rule 5.1.14.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_1_15_enabled | <p>Whether to apply CIS rule 5.1.15.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_1_16_enabled | <p>Whether to apply CIS rule 5.1.16.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_1_17_enabled | <p>Whether to apply CIS rule 5.1.17.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_1_18_enabled | <p>Whether to apply CIS rule 5.1.18.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_1_19_enabled | <p>Whether to apply CIS rule 5.1.19.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_1_20_enabled | <p>Whether to apply CIS rule 5.1.20.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_1_21_enabled | <p>Whether to apply CIS rule 5.1.21.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_1_22_enabled | <p>Whether to apply CIS rule 5.1.22.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_1_23_enabled | <p>Whether to apply CIS rule 5.1.23.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_1_24_enabled | <p>Whether to apply CIS rule 4.2.24.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_sshd_allow_users | <p>The users to allow for SSH.</p> | list of 'str' | no |  | [] |
| rhel8cis_sshd_allow_groups | <p>The groups to allow for SSH.</p> | list of 'str' | no |  | ['wheel'] |
| rhel8cis_sshd_deny_users | <p>The users to deny for SSH.</p> | list of 'str' | no |  | [] |
| rhel8cis_sshd_deny_groups | <p>The groups to deny for SSH.</p> | list of 'str' | no |  | [] |
| rhel8cis_sshd_client_alive_interval | <p>The interval for the client alive messages in seconds.</p> | int | no |  | 15 |
| rhel8cis_sshd_client_alive_count_max | <p>The maximum number of client alive messages.</p> | int | no |  | 3 |
| rhel8cis_sshd_login_grace_time | <p>The login grace time in seconds.</p> | int | no |  | 60 |
| rhel8cis_sshd_max_auth_tries | <p>The maximum number of authentication attempts.</p> | int | no |  | 4 |
| rhel8cis_sshd_max_sessions | <p>The maximum number of sessions.</p> | int | no |  | 10 |
| rhel8cis_sshd_max_startups_before_dropping | <p>The maximum number of startups before dropping.</p> | int | no |  | 10 |
| rhel8cis_sshd_max_startups_drop_percentage | <p>The maximum percentage of startups to drop.</p> | int | no |  | 30 |
| rhel8cis_sshd_max_startups_absolute_maximum | <p>The absolute maximum number of startups.</p> | int | no |  | 60 |
| rhel8cis_sshd_log_level | <p>The log level for SSH.</p> | str | no | <ul><li>INFO</li><li>VERBOSE</li></ul> | INFO |
| rhel8cis_rule_5_2_1_enabled | <p>Whether to apply CIS rule 5.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_2_2_enabled | <p>Whether to apply CIS rule 5.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_2_3_enabled | <p>Whether to apply CIS rule 5.2.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_2_4_enabled | <p>Whether to apply CIS rule 5.2.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_2_4_force | <p>Whether to override the level requirement for CIS rule 5.2.4.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_5_2_5_enabled | <p>Whether to apply CIS rule 5.2.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_2_6_enabled | <p>Whether to apply CIS rule 5.2.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_2_7_enabled | <p>Whether to apply CIS rule 5.2.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_sudo_log_file | <p>The log file for sudo.</p> | path | no |  | /var/log/sudo.log |
| rhel8cis_sudo_authentication_timeout | <p>The authentication timeout for sudo in seconds.</p> | int | no |  | 15 |
| rhel8cis_su_group_name | <p>The group name for the su command.</p> | str | no |  | su |
| rhel8cis_su_group_members | <p>The group members for the su command.</p> | list of 'str' | no |  | ['root'] |
| rhel8cis_rule_5_3_1_1_enabled | <p>Whether to apply CIS rule 5.3.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_3_1_2_enabled | <p>Whether to apply CIS rule 5.3.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_3_3_1_1_enabled | <p>Whether to apply CIS rule 5.3.3.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_3_3_1_2_enabled | <p>Whether to apply CIS rule 5.3.3.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_3_3_1_3_enabled | <p>Whether to apply CIS rule 5.3.3.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_3_3_1_3_force | <p>Whether to override the level requirement for CIS rule 5.3.3.1.3.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_lockout_failed_attempts | <p>The number of failed login attempts before lockout.</p> | int | no |  | 5 |
| rhel8cis_lockout_unlock_time | <p>The time in seconds to unlock the account.</p> | int | no |  | 900 |
| rhel8cis_lockout_root_unlock_time | <p>The time in seconds to unlock the root account.</p> | int | no |  | 900 |
| rhel8cis_rule_5_3_3_2_1_enabled | <p>Whether to apply CIS rule 5.3.3.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_3_3_2_2_enabled | <p>Whether to apply CIS rule 5.3.3.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_3_3_2_3_enabled | <p>Whether to apply CIS rule 5.3.3.2.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_3_3_2_4_enabled | <p>Whether to apply CIS rule 5.3.3.2.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_3_3_2_5_enabled | <p>Whether to apply CIS rule 5.3.3.2.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_3_3_2_6_enabled | <p>Whether to apply CIS rule 5.3.3.2.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_3_3_2_7_enabled | <p>Whether to apply CIS rule 5.3.3.2.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_password_min_changed_characters | <p>The minimum number of changed characters for a new password.</p> | int | no |  | 2 |
| rhel8cis_password_min_length | <p>The minimum length for a new password.</p> | int | no |  | 14 |
| rhel8cis_password_max_repeat_characters | <p>The maximum number of repeated characters for a new password.</p> | int | no |  | 3 |
| rhel8cis_password_max_sequential_characters | <p>The maximum number of sequential characters for a new password.</p> | int | no |  | 3 |
| rhel8cis_rule_5_3_3_3_1_enabled | <p>Whether to apply CIS rule 5.3.3.3.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_3_3_3_2_enabled | <p>Whether to apply CIS rule 5.3.3.3.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_3_3_3_3_enabled | <p>Whether to apply CIS rule 5.3.3.3.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_passwords_remembered | <p>The number of passwords remembered.</p> | int | no |  | 24 |
| rhel8cis_rule_5_3_3_4_1_enabled | <p>Whether to apply CIS rule 5.3.3.4.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_3_3_4_2_enabled | <p>Whether to apply CIS rule 5.3.3.4.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_3_3_4_3_enabled | <p>Whether to apply CIS rule 5.3.3.4.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_3_3_4_4_enabled | <p>Whether to apply CIS rule 5.3.3.4.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_4_1_1_enabled | <p>Whether to apply CIS rule 5.4.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_4_1_2_enabled | <p>Whether to apply CIS rule 5.4.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_4_1_2_force | <p>Whether to override the level requirement for CIS rule 5.4.1.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_5_4_1_3_enabled | <p>Whether to apply CIS rule 5.4.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_4_1_4_enabled | <p>Whether to apply CIS rule 5.4.1.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_4_1_5_enabled | <p>Whether to apply CIS rule 5.4.1.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_4_1_6_enabled | <p>Whether to apply CIS rule 5.4.1.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_password_expiration_days | <p>The number of days before password expiration.</p> | int | no |  | 365 |
| rhel8cis_password_minimum_days | <p>The minimum number of days between password changes.</p> | int | no |  | 1 |
| rhel8cis_password_encryption_algorithm | <p>The encryption algorithm used to encrypt passwords.</p> | str | no | <ul><li>SHA512</li><li>yescrypt</li></ul> | SHA512 |
| rhel8cis_password_expiration_warning_days | <p>The number of days before password expiration warning.</p> | int | no |  | 7 |
| rhel8cis_inactive_password_lock_days | <p>The number of days before inactive password lock.</p> | int | no |  | 30 |
| rhel8cis_rule_5_4_2_1_enabled | <p>Whether to apply CIS rule 5.4.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_4_2_2_enabled | <p>Whether to apply CIS rule 5.4.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_4_2_3_enabled | <p>Whether to apply CIS rule 5.4.2.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_4_2_4_enabled | <p>Whether to apply CIS rule 5.4.2.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_4_2_5_enabled | <p>Whether to apply CIS rule 5.4.2.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_4_2_6_enabled | <p>Whether to apply CIS rule 5.4.2.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_4_2_7_enabled | <p>Whether to apply CIS rule 5.4.2.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_4_2_8_enabled | <p>Whether to apply CIS rule 5.4.2.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_4_3_1_enabled | <p>Whether to apply CIS rule 5.4.3.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_4_3_1_force | <p>Whether to override the level requirement for CIS rule 5.4.3.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_5_4_3_2_enabled | <p>Whether to apply CIS rule 5.4.3.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_5_4_3_3_enabled | <p>Whether to apply CIS rule 5.4.3.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_default_user_shell_timeout_seconds | <p>The default user shell timeout in seconds.</p> | int | no |  | 900 |
| rhel8cis_rule_6_1_1_enabled | <p>Whether to apply CIS rule 6.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_1_2_enabled | <p>Whether to apply CIS rule 6.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_1_3_enabled | <p>Whether to apply CIS rule 6.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_aide_cron_file | <p>The file to use for the AIDE cron job.</p> | path | no |  | /etc/cron.d/aide |
| rhel8cis_aide_cron_hour | <p>The hour to run the AIDE cron job.</p> | int | no |  | 5 |
| rhel8cis_aide_cron_minute | <p>The minute to run the AIDE cron job.</p> | int | no |  | 0 |
| rhel8cis_syslog | <p>The syslog configuration.</p> | str | no | <ul><li>rsyslog</li><li>journald</li></ul> | rsyslog |
| rhel8cis_rule_6_2_1_1_1_enabled | <p>Whether to apply CIS rule 6.2.1.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_2_1_1_2_enabled | <p>Whether to apply CIS rule 6.2.1.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_2_1_1_3_enabled | <p>Whether to apply CIS rule 6.2.1.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_2_1_1_4_enabled | <p>Whether to apply CIS rule 6.2.1.1.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_2_1_1_5_enabled | <p>Whether to apply CIS rule 6.2.1.1.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_2_1_1_6_enabled | <p>Whether to apply CIS rule 6.2.1.1.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_journald_systemmaxuse | <p>The maximum disk usage for the system journal.</p> | str | no |  | 10M |
| rhel8cis_journald_systemkeepfree | <p>The minimum disk space to keep free for the system journal.</p> | str | no |  | 100G |
| rhel8cis_journald_runtimemaxuse | <p>The maximum disk usage for the runtime journal.</p> | str | no |  | 10M |
| rhel8cis_journald_runtimekeepfree | <p>The minimum disk space to keep free for the runtime journal.</p> | str | no |  | 100G |
| rhel8cis_journald_maxfilesec | <p>The maximum file retention time.</p> | str | no |  | 1month |
| rhel8cis_rule_6_2_1_2_1_enabled | <p>Whether to apply CIS rule 6.2.1.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_2_1_2_2_enabled | <p>Whether to apply CIS rule 6.2.1.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_2_1_2_3_enabled | <p>Whether to apply CIS rule 6.2.1.2.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_2_1_2_4_enabled | <p>Whether to apply CIS rule 6.2.1.2.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_remote_log_server | <p>The remote log server to use.</p> | str | no |  |  |
| rhel8cis_journal_server_key_file | <p>The journal server key file.</p> | path | no |  | /etc/ssl/private/journal-upload.pem |
| rhel8cis_journal_server_cert_file | <p>The journal server certificate file.</p> | path | no |  | /etc/ssl/certs/journal-upload.pem |
| rhel8cis_journal_server_trusted_cert_file | <p>The journal server trusted certificate file.</p> | path | no |  | /etc/ssl/ca/trusted.pem |
| rhel8cis_rule_6_2_2_1_enabled | <p>Whether to apply CIS rule 6.2.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_2_2_2_enabled | <p>Whether to apply CIS rule 6.2.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_2_2_3_enabled | <p>Whether to apply CIS rule 6.2.2.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_2_2_4_enabled | <p>Whether to apply CIS rule 6.2.2.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_2_2_5_enabled | <p>Whether to apply CIS rule 6.2.2.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_2_2_6_enabled | <p>Whether to apply CIS rule 6.2.2.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_2_2_7_enabled | <p>Whether to apply CIS rule 6.2.2.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_2_2_8_enabled | <p>Whether to apply CIS rule 6.2.2.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_logrotate_frequency | <p>The logrotate frequency.</p> | str | no | <ul><li>daily</li><li>weekly</li><li>monthly</li></ul> | daily |
| rhel8cis_rule_6_2_3_1_enabled | <p>Whether to apply CIS rule 6.2.3.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_1_1_enabled | <p>Whether to apply CIS rule 6.3.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_1_1_force | <p>Whether to override the level requirement for CIS rule 6.3.1.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_1_2_enabled | <p>Whether to apply CIS rule 6.3.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_1_2_force | <p>Whether to override the level requirement for CIS rule 6.3.1.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_1_3_enabled | <p>Whether to apply CIS rule 6.3.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_1_3_force | <p>Whether to override the level requirement for CIS rule 6.3.1.3.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_1_4_enabled | <p>Whether to apply CIS rule 6.3.1.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_1_4_force | <p>Whether to override the level requirement for CIS rule 6.3.1.4.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_audit_backlog_limit | <p>The audit backlog limit.</p> | int | no |  | 8192 |
| rhel8cis_rule_6_3_2_1_enabled | <p>Whether to apply CIS rule 6.3.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_2_1_force | <p>Whether to override the level requirement for CIS rule 6.3.2.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_2_2_enabled | <p>Whether to apply CIS rule 6.3.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_2_2_force | <p>Whether to override the level requirement for CIS rule 6.3.2.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_2_3_enabled | <p>Whether to apply CIS rule 6.3.2.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_2_3_force | <p>Whether to override the level requirement for CIS rule 6.3.2.3.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_2_4_enabled | <p>Whether to apply CIS rule 6.3.2.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_2_4_force | <p>Whether to override the level requirement for CIS rule 6.3.2.4.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_auditd_max_log_file | <p>The maximum auditd log file size.</p> | int | no |  | 10 |
| rhel8cis_auditd_disk_full_action | <p>The action to take when the auditd disk is full.</p> | str | no | <ul><li>single</li><li>halt</li></ul> | halt |
| rhel8cis_auditd_disk_error_action | <p>The action to take when the auditd disk has an error.</p> | str | no | <ul><li>single</li><li>halt</li><li>syslog</li></ul> | halt |
| rhel8cis_rule_6_3_3_1_enabled | <p>Whether to apply CIS rule 6.3.3.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_3_1_force | <p>Whether to override the level requirement for CIS rule 6.3.3.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_3_2_enabled | <p>Whether to apply CIS rule 6.3.3.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_3_2_force | <p>Whether to override the level requirement for CIS rule 6.3.3.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_3_3_enabled | <p>Whether to apply CIS rule 6.3.3.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_3_3_force | <p>Whether to override the level requirement for CIS rule 6.3.3.3.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_3_4_enabled | <p>Whether to apply CIS rule 6.3.3.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_3_4_force | <p>Whether to override the level requirement for CIS rule 6.3.3.4.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_3_5_enabled | <p>Whether to apply CIS rule 6.3.3.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_3_5_force | <p>Whether to override the level requirement for CIS rule 6.3.3.5.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_3_6_enabled | <p>Whether to apply CIS rule 6.3.3.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_3_6_force | <p>Whether to override the level requirement for CIS rule 6.3.3.6.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_3_7_enabled | <p>Whether to apply CIS rule 6.3.3.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_3_7_force | <p>Whether to override the level requirement for CIS rule 6.3.3.7.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_3_8_enabled | <p>Whether to apply CIS rule 6.3.3.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_3_8_force | <p>Whether to override the level requirement for CIS rule 6.3.3.8.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_3_9_enabled | <p>Whether to apply CIS rule 6.3.3.9.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_3_9_force | <p>Whether to override the level requirement for CIS rule 6.3.3.9.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_3_10_enabled | <p>Whether to apply CIS rule 6.3.3.10.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_3_10_force | <p>Whether to override the level requirement for CIS rule 6.3.3.10.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_3_11_enabled | <p>Whether to apply CIS rule 6.3.3.11.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_3_11_force | <p>Whether to override the level requirement for CIS rule 6.3.3.11.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_3_12_enabled | <p>Whether to apply CIS rule 6.3.3.12.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_3_12_force | <p>Whether to override the level requirement for CIS rule 6.3.3.12.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_3_13_enabled | <p>Whether to apply CIS rule 6.3.3.13.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_3_13_force | <p>Whether to override the level requirement for CIS rule 6.3.3.13.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_3_14_enabled | <p>Whether to apply CIS rule 6.3.3.14.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_3_14_force | <p>Whether to override the level requirement for CIS rule 6.3.3.14.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_3_15_enabled | <p>Whether to apply CIS rule 6.3.3.15.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_3_15_force | <p>Whether to override the level requirement for CIS rule 6.3.3.15.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_3_16_enabled | <p>Whether to apply CIS rule 6.3.3.16.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_3_16_force | <p>Whether to override the level requirement for CIS rule 6.3.3.16.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_3_17_enabled | <p>Whether to apply CIS rule 6.3.3.17.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_3_17_force | <p>Whether to override the level requirement for CIS rule 6.3.3.17.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_3_18_enabled | <p>Whether to apply CIS rule 6.3.3.18.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_3_18_force | <p>Whether to override the level requirement for CIS rule 6.3.3.18.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_3_19_enabled | <p>Whether to apply CIS rule 6.3.3.19.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_3_19_force | <p>Whether to override the level requirement for CIS rule 6.3.3.19.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_3_20_enabled | <p>Whether to apply CIS rule 6.3.3.20.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_3_20_force | <p>Whether to override the level requirement for CIS rule 6.3.3.20.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_3_21_enabled | <p>Whether to apply CIS rule 6.3.3.21.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_3_21_force | <p>Whether to override the level requirement for CIS rule 6.3.3.21.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_3_22_enabled | <p>Whether to apply CIS rule 6.3.3.22.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_3_22_force | <p>Whether to override the level requirement for CIS rule 6.3.3.22.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_4_1_enabled | <p>Whether to apply CIS rule 6.3.4.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_4_1_force | <p>Whether to override the level requirement for CIS rule 6.3.4.1.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_4_2_enabled | <p>Whether to apply CIS rule 6.3.4.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_4_2_force | <p>Whether to override the level requirement for CIS rule 6.3.4.2.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_4_3_enabled | <p>Whether to apply CIS rule 6.3.4.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_4_3_force | <p>Whether to override the level requirement for CIS rule 6.3.4.3.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_4_4_enabled | <p>Whether to apply CIS rule 6.3.4.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_4_4_force | <p>Whether to override the level requirement for CIS rule 6.3.4.4.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_4_5_enabled | <p>Whether to apply CIS rule 6.3.4.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_4_5_force | <p>Whether to override the level requirement for CIS rule 6.3.4.5.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_4_6_enabled | <p>Whether to apply CIS rule 6.3.4.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_4_6_force | <p>Whether to override the level requirement for CIS rule 6.3.4.6.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_4_7_enabled | <p>Whether to apply CIS rule 6.3.4.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_4_7_force | <p>Whether to override the level requirement for CIS rule 6.3.4.7.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_4_8_enabled | <p>Whether to apply CIS rule 6.3.4.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_4_8_force | <p>Whether to override the level requirement for CIS rule 6.3.4.8.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_4_9_enabled | <p>Whether to apply CIS rule 6.3.4.9.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_4_9_force | <p>Whether to override the level requirement for CIS rule 6.3.4.9.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_6_3_4_10_enabled | <p>Whether to apply CIS rule 6.3.4.10.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_6_3_4_10_force | <p>Whether to override the level requirement for CIS rule 6.3.4.10.</p><p>This applies when the machine type is appropriate.</p> | bool | no |  | False |
| rhel8cis_rule_7_1_1_enabled | <p>Whether to apply CIS rule 7.1.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_7_1_2_enabled | <p>Whether to apply CIS rule 7.1.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_7_1_3_enabled | <p>Whether to apply CIS rule 7.1.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_7_1_4_enabled | <p>Whether to apply CIS rule 7.1.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_7_1_5_enabled | <p>Whether to apply CIS rule 7.1.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_7_1_6_enabled | <p>Whether to apply CIS rule 7.1.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_7_1_7_enabled | <p>Whether to apply CIS rule 7.1.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_7_1_8_enabled | <p>Whether to apply CIS rule 7.1.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_7_1_9_enabled | <p>Whether to apply CIS rule 7.1.9.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_7_1_10_enabled | <p>Whether to apply CIS rule 7.1.10.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_7_1_11_enabled | <p>Whether to apply CIS rule 7.1.11.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_7_1_12_enabled | <p>Whether to apply CIS rule 7.1.12.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_7_1_13_enabled | <p>Whether to apply CIS rule 7.1.13.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_7_2_1_enabled | <p>Whether to apply CIS rule 7.2.1.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_7_2_2_enabled | <p>Whether to apply CIS rule 7.2.2.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_7_2_3_enabled | <p>Whether to apply CIS rule 7.2.3.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_7_2_4_enabled | <p>Whether to apply CIS rule 7.2.4.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_7_2_5_enabled | <p>Whether to apply CIS rule 7.2.5.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_7_2_6_enabled | <p>Whether to apply CIS rule 7.2.6.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_7_2_7_enabled | <p>Whether to apply CIS rule 7.2.7.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_7_2_8_enabled | <p>Whether to apply CIS rule 7.2.8.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |
| rhel8cis_rule_7_2_9_enabled | <p>Whether to apply CIS rule 7.2.9.</p><p>This applies when the level and machine type are appropriate.</p> | bool | no |  | True |

### Options for rhel8cis_chrony_servers
|Option|Description|Type|Required|Choices|Default|
|---|---|---|---|---|---|
| name | <p>The NTP server name.</p> | str | yes |  |  |
| options | <p>The NTP server options.</p> | list of 'str' | no |  |  |


## License
MIT

## Author and Project Information
Jim Tarpley (@trippsc2)
<!-- END_ANSIBLE_DOCS -->
