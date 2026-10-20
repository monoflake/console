# Deployment

Nothing deploys on a push any more. The platform this repository deployed to is being replaced by
monoflake/platform, whose model says how an app is built, what artifact it becomes and how it is
deployed; its apps are to be deployed that way, written anew, once it runs. What CI may reach
meanwhile is the workspace's `scripts/`, from a checkout of the workspace at `$WORKSPACE`, built
first with `pnpm exec rescript build`: `scripts/change/deployable` for what a change needs built,
`scripts/deploy/base` and `scripts/deploy/artifact` for the old pipeline's base and bucket.
