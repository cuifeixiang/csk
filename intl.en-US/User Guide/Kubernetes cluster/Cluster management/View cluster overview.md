# View cluster overview {#task_qfb_4c2_vdb .task}

This topic describes how to view the health status of a Kubernetes cluster. Alibaba Cloud Container Service for Kubernetes provides each Kubernetes cluster with the application status, component status, and resource monitoring charts.

1.  Log on to the [Container Service console](https://partners-intl.console.aliyun.com/#/cs). 
2.  In the left-side navigation pane under Kubernetes, click **Overview**. 
3.  Select the target cluster and namespace. You can view the application status, component status, and resource monitoring charts. 

    -   **Application status**: The status of deployments, pods, and replica sets that are currently running. Green indicates the normal status and orange indicates an exception.
    -   **Node status**: Displays the node status of the current cluster.
    -   **Component status**: The components of Kubernetes clusters are generally deployed under the kube-system namespace, including the core components such as scheduler, controller-manager, and etcd.
    -   **Resource monitor**: Provides the monitoring charts of CPU and memory.  CPU is measured in cores and is accurate to three decimal places. The minimum unit is millicores, that is, one thousandth of one core. Memory is measured in G and is accurate to three decimal places.  For more information, see [Meaning of CPU](https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/#meaning-of-cpu) and [Meaning of memory](https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/#meaning-of-memory).
    -   **Event**: Displays event information of the cluster, such as warnings and error events.
    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/18985/155126219210836_en-US.png)


