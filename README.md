# Agregar el repositorio de Bitnami (si no lo tienes)
helm repo add bitnami https://charts.bitnami.com/bitnami
helm repo update

# Cambiar al proyecto nicolas-sierra-dev
oc project nicolas-sierra-dev

# Instalar PostgreSQL
helm install postgresql bitnami/postgresql \
  --namespace nicolas-sierra-dev \
  --values values.yaml