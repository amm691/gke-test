
# CI/CD Pipeline for Deploying Applications on GKE

1. Create two GKE clusters: **dev** .
2. Add Kubernetes manifests to the `kubernetes/` folder.
3. Create `skaffold.yaml`.
4. Create `cloudbuild.yaml` to build and push images to Artifact Registry and configure trigger.
5. Create Cloud Deploy pipeline and targets for **dev** clusters.
6. Push changes to GitHub to trigger the pipeline.

---
Actvity Log:

      + cluster_ipv4_cidr                        = (known after apply)
      + datapath_provider                        = (known after apply)
      + default_max_pods_per_node                = (known after apply)
      + deletion_protection                      = true
      + disable_l4_lb_firewall_reconciliation    = false
      + effective_labels                         = {
          + "goog-terraform-provisioned" = "true"
        }
      + enable_cilium_clusterwide_network_policy = false
      + enable_fqdn_network_policy               = false
      + enable_intranode_visibility              = (known after apply)
      + enable_kubernetes_alpha                  = false
      + enable_l4_ilb_subsetting                 = false
      + enable_legacy_abac                       = false
      + enable_multi_networking                  = false
      + enable_shielded_nodes                    = true
      + endpoint                                 = (known after apply)
      + id                                       = (known after apply)
      + initial_node_count                       = 1
      + label_fingerprint                        = (known after apply)
      + location                                 = "us-central1"
      + logging_service                          = (known after apply)
      + master_version                           = (known after apply)
      + monitoring_service                       = (known after apply)
      + name                                     = "dev-cluster"
      + network                                  = "default"
      + networking_mode                          = (known after apply)
      + node_locations                           = (known after apply)
      + node_version                             = (known after apply)
      + operation                                = (known after apply)
      + private_ipv6_google_access               = (known after apply)
      + project                                  = (known after apply)
      + self_link                                = (known after apply)
      + services_ipv4_cidr                       = (known after apply)
      + subnetwork                               = (known after apply)
      + terraform_labels                         = {
          + "goog-terraform-provisioned" = "true"
        }
      + tpu_ipv4_cidr_block                      = (known after apply)

      + addons_config (known after apply)

      + anonymous_authentication_config (known after apply)

      + authenticator_groups_config (known after apply)

      + cluster_autoscaling (known after apply)

      + confidential_nodes (known after apply)

      + control_plane_endpoints_config (known after apply)

      + cost_management_config (known after apply)

      + database_encryption (known after apply)

      + default_snat_status (known after apply)

      + enterprise_config (known after apply)

      + gateway_api_config (known after apply)

      + gke_auto_upgrade_config (known after apply)

      + identity_service_config (known after apply)

      + ip_allocation_policy (known after apply)

      + logging_config (known after apply)

      + master_auth (known after apply)

      + master_authorized_networks_config (known after apply)

      + mesh_certificates (known after apply)

      + monitoring_config (known after apply)

      + node_config {
          + disk_size_gb     = 50
          + disk_type        = (known after apply)
          + effective_taints = (known after apply)
          + image_type       = (known after apply)
          + labels           = (known after apply)
          + local_ssd_count  = (known after apply)
          + logging_variant  = (known after apply)
          + machine_type     = "e2-medium"
          + metadata         = (known after apply)
          + min_cpu_platform = (known after apply)
          + oauth_scopes     = (known after apply)
          + preemptible      = false
          + service_account  = (known after apply)
          + spot             = false

          + boot_disk (known after apply)

          + confidential_nodes (known after apply)

          + gcfs_config (known after apply)

          + guest_accelerator (known after apply)

          + kubelet_config (known after apply)

          + linux_node_config (known after apply)

          + shielded_instance_config (known after apply)

          + windows_node_config (known after apply)

          + workload_metadata_config (known after apply)
        }

      + node_pool (known after apply)

      + node_pool_auto_config (known after apply)

      + node_pool_defaults (known after apply)

      + notification_config (known after apply)

      + pod_autoscaling (known after apply)

      + rbac_binding_config (known after apply)

      + release_channel (known after apply)

      + security_posture_config (known after apply)

      + service_external_ips_config (known after apply)

      + vertical_pod_autoscaling (known after apply)

      + workload_identity_config (known after apply)
    }

Plan: 1 to add, 0 to change, 0 to destroy.

Changes to Outputs:
  + cluster_endpoint = (known after apply)
  + cluster_name     = "dev-cluster"

─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────── 

Note: You didn't use the -out option to save this plan, so Terraform can't guarantee to take exactly these actions if you run "terraform    
apply" now.
PS C:\Users\Dell\Desktop\Terraform\HCL\HCL_GCP\GKE-1\gke-test\terraform> terraform apply

Terraform used the selected providers to generate the following execution plan. Resource actions are indicated with the following symbols:  
  + create

Terraform will perform the following actions:

  # google_container_cluster.primary will be created
  + resource "google_container_cluster" "primary" {
      + cluster_ipv4_cidr                        = (known after apply)
      + datapath_provider                        = (known after apply)
      + default_max_pods_per_node                = (known after apply)
      + deletion_protection                      = true
      + disable_l4_lb_firewall_reconciliation    = false
      + effective_labels                         = {
          + "goog-terraform-provisioned" = "true"
        }
      + enable_cilium_clusterwide_network_policy = false
      + enable_fqdn_network_policy               = false
      + enable_intranode_visibility              = (known after apply)
      + enable_kubernetes_alpha                  = false
      + enable_l4_ilb_subsetting                 = false
      + enable_legacy_abac                       = false
      + enable_multi_networking                  = false
      + enable_shielded_nodes                    = true
      + endpoint                                 = (known after apply)
      + id                                       = (known after apply)
      + initial_node_count                       = 1
      + label_fingerprint                        = (known after apply)
      + location                                 = "us-central1"
      + logging_service                          = (known after apply)
      + master_version                           = (known after apply)
      + monitoring_service                       = (known after apply)
      + name                                     = "dev-cluster"
      + network                                  = "default"
      + networking_mode                          = (known after apply)
      + node_locations                           = (known after apply)
      + node_version                             = (known after apply)
      + operation                                = (known after apply)
      + private_ipv6_google_access               = (known after apply)
      + project                                  = (known after apply)
      + self_link                                = (known after apply)
      + services_ipv4_cidr                       = (known after apply)
      + subnetwork                               = (known after apply)
      + terraform_labels                         = {
          + "goog-terraform-provisioned" = "true"
        }
      + tpu_ipv4_cidr_block                      = (known after apply)

      + addons_config (known after apply)

      + anonymous_authentication_config (known after apply)

      + authenticator_groups_config (known after apply)

      + cluster_autoscaling (known after apply)

      + confidential_nodes (known after apply)

      + control_plane_endpoints_config (known after apply)

      + cost_management_config (known after apply)

      + database_encryption (known after apply)

      + default_snat_status (known after apply)

      + enterprise_config (known after apply)

      + gateway_api_config (known after apply)

      + gke_auto_upgrade_config (known after apply)

      + identity_service_config (known after apply)

      + ip_allocation_policy (known after apply)

      + logging_config (known after apply)

      + master_auth (known after apply)

      + master_authorized_networks_config (known after apply)

      + mesh_certificates (known after apply)

      + monitoring_config (known after apply)

      + node_config {
          + disk_size_gb     = 50
          + disk_type        = (known after apply)
          + effective_taints = (known after apply)
          + image_type       = (known after apply)
          + labels           = (known after apply)
          + local_ssd_count  = (known after apply)
          + logging_variant  = (known after apply)
          + machine_type     = "e2-medium"
          + metadata         = (known after apply)
          + min_cpu_platform = (known after apply)
          + oauth_scopes     = (known after apply)
          + preemptible      = false
          + service_account  = (known after apply)
          + spot             = false

          + boot_disk (known after apply)

          + confidential_nodes (known after apply)

          + gcfs_config (known after apply)

          + guest_accelerator (known after apply)

          + kubelet_config (known after apply)

          + linux_node_config (known after apply)

          + shielded_instance_config (known after apply)

          + windows_node_config (known after apply)

          + workload_metadata_config (known after apply)
        }

      + node_pool (known after apply)

      + node_pool_auto_config (known after apply)

      + node_pool_defaults (known after apply)

      + notification_config (known after apply)

      + pod_autoscaling (known after apply)

      + rbac_binding_config (known after apply)

      + release_channel (known after apply)

      + security_posture_config (known after apply)

      + service_external_ips_config (known after apply)

      + vertical_pod_autoscaling (known after apply)

      + workload_identity_config (known after apply)
    }

Plan: 1 to add, 0 to change, 0 to destroy.

Changes to Outputs:
  + cluster_endpoint = (known after apply)
  + cluster_name     = "dev-cluster"

Do you want to perform these actions?
  Terraform will perform the actions described above.
  Only 'yes' will be accepted to approve.

  Enter a value:

Apply cancelled.
PS C:\Users\Dell\Desktop\Terraform\HCL\HCL_GCP\GKE-1\gke-test\terraform> terraform apply

Terraform used the selected providers to generate the following execution plan. Resource actions are indicated with the following symbols:  
  + create

Terraform will perform the following actions:

  # google_container_cluster.primary will be created
  + resource "google_container_cluster" "primary" {
      + cluster_ipv4_cidr                        = (known after apply)
      + datapath_provider                        = (known after apply)
      + default_max_pods_per_node                = (known after apply)
      + deletion_protection                      = true
      + disable_l4_lb_firewall_reconciliation    = false
      + effective_labels                         = {
          + "goog-terraform-provisioned" = "true"
        }
      + enable_cilium_clusterwide_network_policy = false
      + enable_fqdn_network_policy               = false
      + enable_intranode_visibility              = (known after apply)
      + enable_kubernetes_alpha                  = false
      + enable_l4_ilb_subsetting                 = false
      + enable_legacy_abac                       = false
      + enable_multi_networking                  = false
      + enable_shielded_nodes                    = true
      + endpoint                                 = (known after apply)
      + id                                       = (known after apply)
      + initial_node_count                       = 1
      + label_fingerprint                        = (known after apply)
      + location                                 = "us-central1"
      + logging_service                          = (known after apply)
      + master_version                           = (known after apply)
      + monitoring_service                       = (known after apply)
      + name                                     = "dev-cluster"
      + network                                  = "default"
      + networking_mode                          = (known after apply)
      + node_locations                           = (known after apply)
      + node_version                             = (known after apply)
      + operation                                = (known after apply)
      + private_ipv6_google_access               = (known after apply)
      + project                                  = (known after apply)
      + self_link                                = (known after apply)
      + services_ipv4_cidr                       = (known after apply)
      + subnetwork                               = (known after apply)
      + terraform_labels                         = {
          + "goog-terraform-provisioned" = "true"
        }
      + tpu_ipv4_cidr_block                      = (known after apply)

      + addons_config (known after apply)

      + anonymous_authentication_config (known after apply)

      + authenticator_groups_config (known after apply)

      + cluster_autoscaling (known after apply)

      + confidential_nodes (known after apply)

      + control_plane_endpoints_config (known after apply)

      + cost_management_config (known after apply)

      + database_encryption (known after apply)

      + default_snat_status (known after apply)

      + enterprise_config (known after apply)

      + gateway_api_config (known after apply)

      + gke_auto_upgrade_config (known after apply)

      + identity_service_config (known after apply)

      + ip_allocation_policy (known after apply)

      + logging_config (known after apply)

      + master_auth (known after apply)

      + master_authorized_networks_config (known after apply)

      + mesh_certificates (known after apply)

      + monitoring_config (known after apply)

      + node_config {
          + disk_size_gb     = 50
          + disk_type        = (known after apply)
          + effective_taints = (known after apply)
          + image_type       = (known after apply)
          + labels           = (known after apply)
          + local_ssd_count  = (known after apply)
          + logging_variant  = (known after apply)
          + machine_type     = "e2-medium"
          + metadata         = (known after apply)
          + min_cpu_platform = (known after apply)
          + oauth_scopes     = (known after apply)
          + preemptible      = false
          + service_account  = (known after apply)
          + spot             = false

          + boot_disk (known after apply)

          + confidential_nodes (known after apply)

          + gcfs_config (known after apply)

          + guest_accelerator (known after apply)

          + kubelet_config (known after apply)

          + linux_node_config (known after apply)

          + shielded_instance_config (known after apply)

          + windows_node_config (known after apply)

          + workload_metadata_config (known after apply)
        }

      + node_pool (known after apply)

      + node_pool_auto_config (known after apply)

      + node_pool_defaults (known after apply)

      + notification_config (known after apply)

      + pod_autoscaling (known after apply)

      + rbac_binding_config (known after apply)

      + release_channel (known after apply)

      + security_posture_config (known after apply)

      + service_external_ips_config (known after apply)

      + vertical_pod_autoscaling (known after apply)

      + workload_identity_config (known after apply)
    }

Plan: 1 to add, 0 to change, 0 to destroy.

Changes to Outputs:
  + cluster_endpoint = (known after apply)
  + cluster_name     = "dev-cluster"

Do you want to perform these actions?
  Terraform will perform the actions described above.
  Only 'yes' will be accepted to approve.

  Enter a value: yes

google_container_cluster.primary: Creating...
╷
│ Error: googleapi: Error 403: Required "container.clusters.create" permission(s) for "projects/fleet-purpose-467517-g6/locations/us-central1/clusters/dev-cluster".
│ Details:
│ [
│   {
│     "@type": "type.googleapis.com/google.rpc.RequestInfo",
│     "requestId": "0x32353108e084583a"
│   },
│   {
│     "@type": "type.googleapis.com/google.rpc.ErrorInfo",
│     "domain": "container.googleapis.com",
│     "reason": "IAM_PERMISSION_DENIED"
│   }
│ ]
│ , forbidden
│
│   with google_container_cluster.primary,
│   on gke.tf line 1, in resource "google_container_cluster" "primary":
│    1: resource "google_container_cluster" "primary" {
│
╵
PS C:\Users\Dell\Desktop\Terraform\HCL\HCL_GCP\GKE-1\gke-test\terraform> 
PS C:\Users\Dell\Desktop\Terraform\HCL\HCL_GCP\GKE-1\gke-test\terraform> terraform plan

Terraform used the selected providers to generate the following execution plan. Resource actions are indicated with the following symbols:  
  + create

Terraform will perform the following actions:

  # google_container_cluster.primary will be created
  + resource "google_container_cluster" "primary" {
      + cluster_ipv4_cidr                        = (known after apply)
      + datapath_provider                        = (known after apply)
      + default_max_pods_per_node                = (known after apply)
      + deletion_protection                      = true
      + disable_l4_lb_firewall_reconciliation    = false
      + effective_labels                         = {
          + "goog-terraform-provisioned" = "true"
        }
      + enable_cilium_clusterwide_network_policy = false
      + enable_fqdn_network_policy               = false
      + enable_intranode_visibility              = (known after apply)
      + enable_kubernetes_alpha                  = false
      + enable_l4_ilb_subsetting                 = false
      + enable_legacy_abac                       = false
      + enable_multi_networking                  = false
      + enable_shielded_nodes                    = true
      + endpoint                                 = (known after apply)
      + id                                       = (known after apply)
      + initial_node_count                       = 1
      + label_fingerprint                        = (known after apply)
      + location                                 = "us-central1"
      + logging_service                          = (known after apply)
      + master_version                           = (known after apply)
      + monitoring_service                       = (known after apply)
      + name                                     = "dev-cluster"
      + network                                  = "default"
      + networking_mode                          = (known after apply)
      + node_locations                           = (known after apply)
      + node_version                             = (known after apply)
      + operation                                = (known after apply)
      + private_ipv6_google_access               = (known after apply)
      + project                                  = (known after apply)
      + self_link                                = (known after apply)
      + services_ipv4_cidr                       = (known after apply)
      + subnetwork                               = (known after apply)
      + terraform_labels                         = {
          + "goog-terraform-provisioned" = "true"
        }
      + tpu_ipv4_cidr_block                      = (known after apply)

      + addons_config (known after apply)

      + anonymous_authentication_config (known after apply)

      + authenticator_groups_config (known after apply)

      + cluster_autoscaling (known after apply)

      + confidential_nodes (known after apply)

      + control_plane_endpoints_config (known after apply)

      + cost_management_config (known after apply)

      + database_encryption (known after apply)

      + default_snat_status (known after apply)

      + enterprise_config (known after apply)

      + gateway_api_config (known after apply)

      + gke_auto_upgrade_config (known after apply)

      + identity_service_config (known after apply)

      + ip_allocation_policy (known after apply)

      + logging_config (known after apply)

      + master_auth (known after apply)

      + master_authorized_networks_config (known after apply)

      + mesh_certificates (known after apply)

      + monitoring_config (known after apply)

      + node_config {
          + disk_size_gb     = 50
          + disk_type        = (known after apply)
          + effective_taints = (known after apply)
          + image_type       = (known after apply)
          + labels           = (known after apply)
          + local_ssd_count  = (known after apply)
          + logging_variant  = (known after apply)
          + machine_type     = "e2-medium"
          + metadata         = (known after apply)
          + min_cpu_platform = (known after apply)
          + oauth_scopes     = (known after apply)
          + preemptible      = false
          + service_account  = (known after apply)
          + spot             = false

          + boot_disk (known after apply)

          + confidential_nodes (known after apply)

          + gcfs_config (known after apply)

          + guest_accelerator (known after apply)

          + kubelet_config (known after apply)

          + linux_node_config (known after apply)

          + shielded_instance_config (known after apply)

          + windows_node_config (known after apply)

          + workload_metadata_config (known after apply)
        }

      + node_pool (known after apply)

      + node_pool_auto_config (known after apply)

      + node_pool_defaults (known after apply)

      + notification_config (known after apply)

      + pod_autoscaling (known after apply)

      + rbac_binding_config (known after apply)

      + release_channel (known after apply)

      + security_posture_config (known after apply)

      + service_external_ips_config (known after apply)

      + vertical_pod_autoscaling (known after apply)

      + workload_identity_config (known after apply)
    }

Plan: 1 to add, 0 to change, 0 to destroy.

Changes to Outputs:
  + cluster_endpoint = (known after apply)

─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────── 

Note: You didn't use the -out option to save this plan, so Terraform can't guarantee to take exactly these actions if you run "terraform    
apply" now.
PS C:\Users\Dell\Desktop\Terraform\HCL\HCL_GCP\GKE-1\gke-test\terraform> terraform apply

Terraform used the selected providers to generate the following execution plan. Resource actions are indicated with the following symbols:  
  + create

Terraform will perform the following actions:

  # google_container_cluster.primary will be created
  + resource "google_container_cluster" "primary" {
      + cluster_ipv4_cidr                        = (known after apply)
      + datapath_provider                        = (known after apply)
      + default_max_pods_per_node                = (known after apply)
      + deletion_protection                      = true
      + disable_l4_lb_firewall_reconciliation    = false
      + effective_labels                         = {
          + "goog-terraform-provisioned" = "true"
        }
      + enable_cilium_clusterwide_network_policy = false
      + enable_fqdn_network_policy               = false
      + enable_intranode_visibility              = (known after apply)
      + enable_kubernetes_alpha                  = false
      + enable_l4_ilb_subsetting                 = false
      + enable_legacy_abac                       = false
      + enable_multi_networking                  = false
      + enable_shielded_nodes                    = true
      + endpoint                                 = (known after apply)
      + id                                       = (known after apply)
      + initial_node_count                       = 1
      + label_fingerprint                        = (known after apply)
      + location                                 = "us-central1"
      + logging_service                          = (known after apply)
      + master_version                           = (known after apply)
      + monitoring_service                       = (known after apply)
      + name                                     = "dev-cluster"
      + network                                  = "default"
      + networking_mode                          = (known after apply)
      + node_locations                           = (known after apply)
      + node_version                             = (known after apply)
      + operation                                = (known after apply)
      + private_ipv6_google_access               = (known after apply)
      + project                                  = (known after apply)
      + self_link                                = (known after apply)
      + services_ipv4_cidr                       = (known after apply)
      + subnetwork                               = (known after apply)
      + terraform_labels                         = {
          + "goog-terraform-provisioned" = "true"
        }
      + tpu_ipv4_cidr_block                      = (known after apply)

      + addons_config (known after apply)

      + anonymous_authentication_config (known after apply)

      + authenticator_groups_config (known after apply)

      + cluster_autoscaling (known after apply)

      + confidential_nodes (known after apply)

      + control_plane_endpoints_config (known after apply)

      + cost_management_config (known after apply)

      + database_encryption (known after apply)

      + default_snat_status (known after apply)

      + enterprise_config (known after apply)

      + gateway_api_config (known after apply)

      + gke_auto_upgrade_config (known after apply)

      + identity_service_config (known after apply)

      + ip_allocation_policy (known after apply)

      + logging_config (known after apply)

      + master_auth (known after apply)

      + master_authorized_networks_config (known after apply)

      + mesh_certificates (known after apply)

      + monitoring_config (known after apply)

      + node_config {
          + disk_size_gb     = 50
          + disk_type        = (known after apply)
          + effective_taints = (known after apply)
          + image_type       = (known after apply)
          + labels           = (known after apply)
          + local_ssd_count  = (known after apply)
          + logging_variant  = (known after apply)
          + machine_type     = "e2-medium"
          + metadata         = (known after apply)
          + min_cpu_platform = (known after apply)
          + oauth_scopes     = (known after apply)
          + preemptible      = false
          + service_account  = (known after apply)
          + spot             = false

          + boot_disk (known after apply)

          + confidential_nodes (known after apply)

          + gcfs_config (known after apply)

          + guest_accelerator (known after apply)

          + kubelet_config (known after apply)

          + linux_node_config (known after apply)

          + shielded_instance_config (known after apply)

          + windows_node_config (known after apply)

          + workload_metadata_config (known after apply)
        }

      + node_pool (known after apply)

      + node_pool_auto_config (known after apply)

      + node_pool_defaults (known after apply)

      + notification_config (known after apply)

      + pod_autoscaling (known after apply)

      + rbac_binding_config (known after apply)

      + release_channel (known after apply)

      + security_posture_config (known after apply)

      + service_external_ips_config (known after apply)

      + vertical_pod_autoscaling (known after apply)

      + workload_identity_config (known after apply)
    }

Plan: 1 to add, 0 to change, 0 to destroy.

Changes to Outputs:
  + cluster_endpoint = (known after apply)

Do you want to perform these actions?
  Terraform will perform the actions described above.
  Only 'yes' will be accepted to approve.

  Enter a value: yes

google_container_cluster.primary: Creating...
╷
│ Error: googleapi: Error 403: Required "container.clusters.create" permission(s) for "projects/fleet-purpose-467517-g6/locations/us-central1/clusters/dev-cluster".
│ Details:
│ [
│   {
│     "@type": "type.googleapis.com/google.rpc.RequestInfo",
│     "requestId": "0xd34813bb92fbce15"
│   },
│   {
│     "@type": "type.googleapis.com/google.rpc.ErrorInfo",
│     "domain": "container.googleapis.com",
│     "reason": "IAM_PERMISSION_DENIED"
│   }
│ ]
│ , forbidden
│
│   with google_container_cluster.primary,
│   on gke.tf line 1, in resource "google_container_cluster" "primary":
│    1: resource "google_container_cluster" "primary" {
│
╵
PS C:\Users\Dell\Desktop\Terraform\HCL\HCL_GCP\GKE-1\gke-test\terraform> terraform apply

Terraform used the selected providers to generate the following execution plan. Resource actions are indicated with the following symbols:  
  + create

Terraform will perform the following actions:

  # google_container_cluster.primary will be created
  + resource "google_container_cluster" "primary" {
      + cluster_ipv4_cidr                        = (known after apply)
      + datapath_provider                        = (known after apply)
      + default_max_pods_per_node                = (known after apply)
      + deletion_protection                      = true
      + disable_l4_lb_firewall_reconciliation    = false
      + effective_labels                         = {
          + "goog-terraform-provisioned" = "true"
        }
      + enable_cilium_clusterwide_network_policy = false
      + enable_fqdn_network_policy               = false
      + enable_intranode_visibility              = (known after apply)
      + enable_kubernetes_alpha                  = false
      + enable_l4_ilb_subsetting                 = false
      + enable_legacy_abac                       = false
      + enable_multi_networking                  = false
      + enable_shielded_nodes                    = true
      + endpoint                                 = (known after apply)
      + id                                       = (known after apply)
      + initial_node_count                       = 1
      + label_fingerprint                        = (known after apply)
      + location                                 = "us-central1"
      + logging_service                          = (known after apply)
      + master_version                           = (known after apply)
      + monitoring_service                       = (known after apply)
      + name                                     = "dev-cluster"
      + network                                  = "default"
      + networking_mode                          = (known after apply)
      + node_locations                           = (known after apply)
      + node_version                             = (known after apply)
      + operation                                = (known after apply)
      + private_ipv6_google_access               = (known after apply)
      + project                                  = (known after apply)
      + self_link                                = (known after apply)
      + services_ipv4_cidr                       = (known after apply)
      + subnetwork                               = (known after apply)
      + terraform_labels                         = {
          + "goog-terraform-provisioned" = "true"
        }
      + tpu_ipv4_cidr_block                      = (known after apply)

      + addons_config (known after apply)

      + anonymous_authentication_config (known after apply)

      + authenticator_groups_config (known after apply)

      + cluster_autoscaling (known after apply)

      + confidential_nodes (known after apply)

      + control_plane_endpoints_config (known after apply)

      + cost_management_config (known after apply)

      + database_encryption (known after apply)

      + default_snat_status (known after apply)

      + enterprise_config (known after apply)

      + gateway_api_config (known after apply)

      + gke_auto_upgrade_config (known after apply)

      + identity_service_config (known after apply)

      + ip_allocation_policy (known after apply)

      + logging_config (known after apply)

      + master_auth (known after apply)

      + master_authorized_networks_config (known after apply)

      + mesh_certificates (known after apply)

      + monitoring_config (known after apply)

      + node_config {
          + disk_size_gb     = 50
          + disk_type        = (known after apply)
          + effective_taints = (known after apply)
          + image_type       = (known after apply)
          + labels           = (known after apply)
          + local_ssd_count  = (known after apply)
          + logging_variant  = (known after apply)
          + machine_type     = "e2-medium"
          + metadata         = (known after apply)
          + min_cpu_platform = (known after apply)
          + oauth_scopes     = (known after apply)
          + preemptible      = false
          + service_account  = (known after apply)
          + spot             = false

          + boot_disk (known after apply)

          + confidential_nodes (known after apply)

          + gcfs_config (known after apply)

          + guest_accelerator (known after apply)

          + kubelet_config (known after apply)

          + linux_node_config (known after apply)

          + shielded_instance_config (known after apply)

          + windows_node_config (known after apply)

          + workload_metadata_config (known after apply)
        }

      + node_pool (known after apply)

      + node_pool_auto_config (known after apply)

      + node_pool_defaults (known after apply)

      + notification_config (known after apply)

      + pod_autoscaling (known after apply)

      + rbac_binding_config (known after apply)

      + release_channel (known after apply)

      + security_posture_config (known after apply)

      + service_external_ips_config (known after apply)

      + vertical_pod_autoscaling (known after apply)

      + workload_identity_config (known after apply)
    }

Plan: 1 to add, 0 to change, 0 to destroy.

Changes to Outputs:
  + cluster_endpoint = (known after apply)

Do you want to perform these actions?
  Terraform will perform the actions described above.
  Only 'yes' will be accepted to approve.

  Enter a value: yes

google_container_cluster.primary: Creating...
google_container_cluster.primary: Still creating... [00m10s elapsed]
google_container_cluster.primary: Still creating... [00m20s elapsed]
google_container_cluster.primary: Still creating... [00m30s elapsed]
google_container_cluster.primary: Still creating... [00m40s elapsed]
google_container_cluster.primary: Still creating... [00m50s elapsed]
google_container_cluster.primary: Still creating... [01m00s elapsed]
google_container_cluster.primary: Still creating... [01m10s elapsed]
google_container_cluster.primary: Still creating... [01m20s elapsed]
google_container_cluster.primary: Still creating... [01m30s elapsed]
google_container_cluster.primary: Still creating... [01m40s elapsed]
google_container_cluster.primary: Still creating... [01m50s elapsed]
google_container_cluster.primary: Still creating... [02m00s elapsed]
google_container_cluster.primary: Still creating... [02m10s elapsed]
google_container_cluster.primary: Still creating... [02m20s elapsed]
google_container_cluster.primary: Still creating... [02m30s elapsed]
google_container_cluster.primary: Still creating... [02m40s elapsed]
google_container_cluster.primary: Still creating... [02m50s elapsed]
google_container_cluster.primary: Still creating... [03m00s elapsed]
google_container_cluster.primary: Still creating... [03m10s elapsed]
google_container_cluster.primary: Still creating... [03m20s elapsed]
google_container_cluster.primary: Still creating... [03m30s elapsed]
google_container_cluster.primary: Still creating... [03m40s elapsed]
google_container_cluster.primary: Still creating... [03m50s elapsed]
google_container_cluster.primary: Still creating... [04m00s elapsed]
google_container_cluster.primary: Still creating... [04m10s elapsed]
google_container_cluster.primary: Still creating... [04m20s elapsed]
google_container_cluster.primary: Still creating... [04m30s elapsed]
google_container_cluster.primary: Still creating... [04m40s elapsed]
google_container_cluster.primary: Still creating... [04m50s elapsed]
google_container_cluster.primary: Still creating... [05m00s elapsed]
google_container_cluster.primary: Still creating... [05m10s elapsed]
google_container_cluster.primary: Still creating... [05m20s elapsed]
google_container_cluster.primary: Creation complete after 5m25s [id=projects/fleet-purpose-467517-g6/locations/us-central1/clusters/dev-cluster]

Apply complete! Resources: 1 added, 0 changed, 0 destroyed.

Outputs:

cluster_endpoint = "34.10.219.221"
cluster_name = "dev-cluster"
PS C:\Users\Dell\Desktop\Terraform\HCL\HCL_GCP\GKE-1\gke-test\terraform>


