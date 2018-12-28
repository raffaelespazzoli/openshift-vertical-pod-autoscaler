# Vertical Pod Autoscaler

## Installation

Run the following:

```
oc new-project vertical-pod-autoscaler
helm template ./charts/vertical-pod-autoscaler --namespace vertical-pod-autoscaler --set vpa_admission_controller.image=quay.io/raffaelespazzoli/vpa-admission-controller --set vpa_admission_controller.tag=latest | oc apply -f -
```

to test it run the following
```
oc apply -f test/vpa.yaml -n vertical-pod-autoscaler
```