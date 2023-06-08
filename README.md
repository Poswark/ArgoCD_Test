# Desafío: Implementación avanzada de ArgoCD con Kubernetes

## Descripción del desafío:
El desafío consiste en implementar un flujo de CI/CD completo utilizando ArgoCD y Kubernetes, centrándose en características y casos de uso avanzados. Los participantes deben construir y desplegar una aplicación en un clúster de Kubernetes utilizando ArgoCD, y demostrar su capacidad para automatizar y gestionar el ciclo de vida de la aplicación de manera eficiente.

## Requisitos y criterios de evaluación:

1. Crear una rama del repositorio {XXXXX} que contenga una aplicación de ejemplo se deja la aplicación HelloWord en springboot
2. Configurar un clúster de Kubernetes y desplegar ArgoCD en el clúster.
3. Configurar un pipeline de CI/CD utilizando Jenkins como CI.
4. Utilizar ArgoCD para gestionar el despliegue y la implementación continua de la aplicación en el clúster de Kubernetes.
5. Demostrar la capacidad de rollback (reversión) en caso de fallos en la implementación.  (FINAL)
6. Implementar características avanzadas de ArgoCD, como la gestión de entornos (dev, staging, producción), la promoción de cambios entre entornos y la configuración de políticas de implementación.


Los equipos serán evaluados en función de los siguientes criterios:

- Complejidad y sofisticación de la solución implementada.
- Calidad del código y las configuraciones utilizadas.
- Eficiencia y escalabilidad de la implementación.
- Utilización efectiva de las características avanzadas de ArgoCD.
- Presentación y capacidad para comunicar el flujo de trabajo y los resultados alcanzados.


# Ayuda Instalación 


Instalar ArgoCD 

```bash
kubectl apply -n argocd -f install_argocd.yaml
```

Revisar los servicios 
```bash
kubectl patch svc argocd-server -n argocd -p '{"spec": {"type": "LoadBalancer"}}'
```

```bash
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d
```


# Link Repositorio 

# 