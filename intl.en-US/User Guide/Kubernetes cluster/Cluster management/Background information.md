# Notice about fixed Kubernetes dashboard vulnerability CVE-2018-18264 {#concept_e3s_hzl_jgb .concept}

Alibaba Cloud Container Service for Kubernetes has fixed dashboard vulnerability CVE-2018-18264. This topic describes the dashboard versions affected by the vulnerability and how to fix the vulnerability. The Kubernetes dashboards that are built in Alibaba Cloud Container Service for Kubernetes are not affected by this vulnerability because they work in the hosted form and their security settings were upgraded before the vulnerability occurred.

## Background information {#section_qt2_nzl_jgb .section}

A security vulnerability, that is, CVE-2018-18264, was discovered in Kubernetes dashboards of V1.10 and earlier versions. This vulnerability allowed attackers to bypass identity authentication and read secrets within the cluster by using the dashboard logon account.

The Kubernetes dashboards that are built in Alibaba Cloud Container Service for Kubernetes are not affected by this vulnerability because they work in the hosted form and their security settings were upgraded before the vulnerability occurred.

For more information about security vulnerability CVE-2018-18264, see:

-   [https://github.com/kubernetes/dashboard/pull/3289](https://github.com/kubernetes/dashboard/pull/3289)
-   [https://github.com/kubernetes/dashboard/pull/3400](https://github.com/kubernetes/dashboard/pull/3400)
-   [https://github.com/kubernetes/dashboard/releases/tag/v1.10.1](https://github.com/kubernetes/dashboard/releases/tag/v1.10.1)

## Conditions required to determine that a Kubernetes dashboard is vulnerable {#section_oh3_d1m_jgb .section}

Your dashboard is vulnerable if you have independently deployed Kubernetes dashboard V1.10 or earlier versions \(V1.7.0 to V1.10.0\) that supports the logon function in your Kubernetes cluster, and you have used custom certificates.

## Resolution {#section_ik2_g1m_jgb .section}

-   If you do not need a dashboard that is deployed independently, run the following command to remove the Kubernetes dashboard from your cluster:

```
kubectl --namespace kube-system delete deployment kubernetes-dashboard
```

-   If you need an independently deployed dashboard, upgrade your dashboard to V1.10.1. For more information, see [https://github.com/kubernetes/dashboard/releases/tag/v1.10.1](https://github.com/kubernetes/dashboard/releases/tag/v1.10.1).

-   If you use the dashboard hosted by Alibaba Cloud Container Service for Kubernetes, you can continue to use your dashboard in the Container Service console because the dashboard was upgraded before the vulnerability occurred.


