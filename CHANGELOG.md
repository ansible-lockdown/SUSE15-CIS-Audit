# Changes to SUSE15-CIS-Audit

# Based on CIS v2.0.1

# 2026 May QA Updates
- Fix benchmark_version: corrected to 'v2.0.1' (was '2.0.0')
- Fix run_audit.sh BENCHMARK_VER: added v prefix (was '2.0.1')
- Fix LICENSE: copyright year updated to 2026, MindPoint capitalisation corrected
- Fix section_6/cis_6.2.3/cis_6.2.3.1.2.yml: goss test guarded on rule_6_2_3_1_1 instead of rule_6_2_3_1_2
- Fix goss.yml: section_1/cis_1.8/*.yml glob was missing `: {}` value
- Fix goss.yml: added missing section_5/cis_5.3.1/*.yml glob (directory existed but was never included)
- Fix templates/ansible_vars_goss.yml.j2: uncommented suse15cis_remote_log_host (was commented out; referenced by cis_6.2.3.1.1 goss test)
- Removed rule_1_1_1_10, rule_2_2_6, rule_2_3_3_3, rule_7_2_10 from vars/CIS.yml (none exist in benchmark v2.0.1)
- Fixed 36 goss test title: fields to match benchmark v2.0.1 wording: "permissions on" -> "access to" (2.4.1.x, 5.1.1-3), "SSH" -> "sshd" (5.1.7/12/17/18/19/20/21), "recorded" -> "collected" (6.3.3.15-18), "are configured" -> "is configured" (7.1.4-10), typo "recieve" -> "receive" (6.2.3.1.2), and others
- Contributing added
- updated run_audit.sh for less risk of incorrect OS being discovered
- suse15cis_firewall variable renamed to suse15cis_firewall_package inline with remediation
