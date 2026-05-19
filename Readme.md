# Book Shop CI/CD Project (Solo Student / Majd Daoudieh)

## Branch Strategies
- **Dev (Port 80):** Artifact-First philosophy. Builds archive, commits to repo, then builds image.
- **Test (Port 81):** Image-First philosophy. Rebuilds from source and pushes to ECR.
- **Prod (Port 82):** Promotion-Only philosophy. Pulls version from IMAGE_VERSION variable.

## Coexistence
All three environments run simultaneously on this EC2 instance at ports 80, 81, and 82.