# Kyverno CEL Policy Migration

This repository demonstrates the migration from traditional Kyverno policies to new CEL-based policy types in the v1alpha1 API version that provide enhanced expressiveness, better performance, and native Kubernetes integration.

## Migrations Done

1. `kubevirt/`: Migrated KubeVirt policy to CEL-based policy type
   - `add-services`: [clusterpolicy](kubevirt/add-services/clusterpolicy.yaml) -> [generatingpolicy](kubevirt/add-services/generatingpolicy.yaml)
2. `karpenter`: Migrated Karpenter policy to CEL-based policy type
   - `add-karpenter`: [clusterpolicy](karpenter/add-karpenter-daemonset-priority-class/clusterpolicy.yaml) -> [mutatingpolicy](karpenter/add-karpenter-daemonset-priority-class/mutatingpolicy.yaml)
   - `add-karpenter-donot-evict`: [clusterpolicy](karpenter/add-karpenter-donot-evict/clusterpolicy.yaml) -> [mutatingpolicy](karpenter/add-karpenter-donot-evict/mutatingpolicy.yaml)
   - `add-karpenter-nodeselector`: [clusterpolicy](karpenter/add-karpenter-nodeselector/clusterpolicy.yaml) -> [mutatingpolicy](karpenter/add-karpenter-nodeselector/mutatingpolicy.yaml)
   - `set-karpenter-non-cpu-limits`: [clusterpolicy](karpenter/set-karpenter-non-cpu-limits/clusterpolicy.yaml) -> [mutatingpolicy](karpenter/set-karpenter-non-cpu-limits/mutatingpolicy.yaml)
3. `add-ns-quota`: Migrated namespace quota policy to CEL-based policy type
   - [clusterpolicy](add-ns-quota/kyverno-add-ns-quota-clusterpolicy.yaml) split into:
       - [limitrange-generatingpolicy](add-ns-quota/kyverno-add-ns-limitrange-generatingpolicy.yaml)
       - [resourcequota-generatingpolicy](add-ns-quota/kyverno-add-ns-resourcequota-generatingpolicy.yaml)
