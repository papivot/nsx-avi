# nsx-avi

```bash
curl -k -u admin --location --request PUT 'https://nsxt01.h2o-4-24842.h2o.vmware.com/policy/api/v1/infra/alb-onboarding-workflow' \
--header 'X-Allow-Overwrite: True' \
--header 'Content-Type: application/json' \
--data-raw '{
"owned_by": "LCM",
"cluster_ip": "10.220.39.34",
"infra_admin_username" : "admin",
"infra_admin_password" : "password",
"dns_servers": ["10.220.136.2"],
"ntp_servers": ["time1.oc.vmware.com"]
}'

Enter host password for user 'admin':
```

```bash
curl -k -u admin --location --request GET 'https://nsxt01.h2o-4-24842.h2o.vmware.com/policy/api/v1/infra/sites/default/enforcement-points/alb-endpoint'
Enter host password for user 'admin':
```

```json
{
  "connection_info" : {
    "username" : "\u0000\u0000\u0000\u0000\u0000\u0000\u0000\u0000",
    "tenant" : "admin",
    "expires_at" : "2024-06-14T07:33:09.960Z",
    "managed_by" : "LCM",
    "status" : "DEACTIVATE_PROVIDER",
    "certificate" : "-----BEGIN CERTIFICATE-----\nMIIDATCCAemgAwIBAgIUCSnlfHBmqlaoZxvfDmrUhpz380YwDQYJKoZIhvcNAQEL\nBQAwMDEuMCwGA1UEAwwlbnN4dDAxLWFsYi5oMm8tNC0yNDg0Mi5oMm8udm13YXJl\nLmNvbTAeFw0yNDA2MTQwMTA5NTZaFw0yNTA2MTQwMTA5NTZaMDAxLjAsBgNVBAMM\nJW5zeHQwMS1hbGIuaDJvLTQtMjQ4NDIuaDJvLnZtd2FyZS5jb20wggEiMA0GCSqG\nSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDW2Eyyg4HAYudAIyBoqkXZQGw3FwpECfuJ\n6TAjaFoMty+B/vdgfe+m59Cr4RywjsBACaLAKRRirHLhU/tU5G4GAn74ZjIBKLaa\nMku2XFnD3K42dVxO2hYLYb7Bw21sQpEH/G82KmW49Fvz5G31MEY9h2uYgcuney93\n3GPtde19jmiMNY5Z+lvwcw/uVr/9LBVfZlarIUBF1RXA2oEV6PX+/82S1YMNu+bO\neLoL4SW0YgC8+1iKFadmJ5RRJ/Jtq/CAHBtv2vUDE8QpoujHVEfYG/9DbqPxXGIc\nRQZ4h5nok2d/wCcgVqdQyO9aa7EsFY9D5VkUt2ZkWQSS1mihy2kZAgMBAAGjEzAR\nMA8GA1UdEQQIMAaHBArcJyIwDQYJKoZIhvcNAQELBQADggEBAASWwfzIpg1q1tBT\nSMuxvvDuV7/dPSeizCSoA23GAbnJ5mz0uub+3mLx822MxOtq1UFbB1z5GJJKpdap\nqYIS8wCvKXp9oOm8+oXXEQUz79H/YpuVrxqo34B2lhjGuGFRw90UYemB26U45V0k\nOQMayaFNJIzX9oya11tqK3Y8aAAWNwcG6+Np2tL+hydqc9X0BlT4Gar7tv3JtOv9\nH5K5RL91sXrwMDPMZ4+lDyO3FUYGDVqm+2LdukxoE0Yn8HdKV6zLQmSaTqOYky+C\nv86xXYT442GdvPNKrEf39ImmWkZ4hy2dWSqu8n8QjJIdBwrNtEXbUGj0NtIkq0/S\nY2MddhQ=\n-----END CERTIFICATE-----\n",
    "is_default_cert" : true,
    "enforcement_point_address" : "10.220.39.34",
    "resource_type" : "AviConnectionInfo"
  },
  "auto_enforce" : true,
  "resource_type" : "EnforcementPoint",
  "id" : "alb-endpoint",
  "display_name" : "alb-endpoint",
  "path" : "/infra/sites/default/enforcement-points/alb-endpoint",
  "relative_path" : "alb-endpoint",
  "parent_path" : "/infra/sites/default",
  "remote_path" : "",
  "unique_id" : "ab78d554-2b08-451a-994d-dc6bb358b4f5",
  "realization_id" : "ab78d554-2b08-451a-994d-dc6bb358b4f5",
  "owner_id" : "8a33ff32-599f-4577-a348-a046135cda7b",
  "marked_for_delete" : false,
  "overridden" : false,
  "_create_time" : 1718328790216,
  "_create_user" : "admin",
  "_last_modified_time" : 1718328790216,
  "_last_modified_user" : "admin",
  "_system_owned" : false,
  "_protection" : "NOT_PROTECTED",
  "_revision" : 0
}
```