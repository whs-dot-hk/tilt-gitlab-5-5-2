analytics_settings(enable = False)

def create_namespace(name):
    k8s_yaml(blob("""apiVersion: v1
kind: Namespace
metadata:
  name: %s
""" % name))

name = "gitlab"

create_namespace(name)

k8s_yaml(helm("charts/gitlab", name, namespace = name, values = "values.yaml"))
