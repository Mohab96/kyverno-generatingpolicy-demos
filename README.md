# Kyverno CEL Policy Migration

Repository demonstrating migration from traditional Kyverno policies to new CEL-based policy types.

## Contents

- `add-ns-quota/`: Original Kyverno v1 policy for adding resource quotas to namespaces
- `kubevirt/`: Original Kyverno v1 policy for KubeVirt

## Migration Example

1. [add-ns-quota](add-ns-quota/kyverno-add-ns-quota.yaml) - Original Kyverno v1 policy
- Split into multiple CEL-based policies:
   - [add-ns-quota-limitrange](add-ns-quota/add-ns-limitrange.yaml)
    - [add-ns-quota-resourcequota](add-ns-quota/add-ns-resourcequota.yaml)

2. [kubevirt-add-services](kubevirt/kyverno-add-services.yaml) - Original Kyverno v1 policy
- Changed to CEL-based policy:
   - [kubevirt-add-services-generating-policy](kubevirt/add-services-generating-policy.yaml)