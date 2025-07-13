# dokploy-update-image-action

This github action updates the image of a dokploy deployment.

## Usage

Add to your Github CI yaml file:

```yaml
...
    steps:
      - name: Dokploy Update Image
        uses: jegork/dokploy-update-image-action@0.1.0
        with:
          token: ${{ secrets.DOKPLOY_TOKEN }} # generate in dokploy settings
          application_id: ${{ secrets.DOKPLOY_APP_ID }} # retrieve from https://my-dokploy-instance.com/api/project.all
          image: ${{ steps.meta.outputs.tags }} # eg. ghcr.io/jegork/my-app:latest
          base_url: ${{ secrets.DOKPLOY_URL }} # https://my-dokploy-instance.com
...
```
