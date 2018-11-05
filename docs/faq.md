# Frequently Asked Questions

## Can I use this on Mac/Windows/Linux?

We're aware of several developers using MageDocker across all major operating systems. This project is pretty near to native Docker experience, so if docker requires some configuration for your OS, MageDocker will most likely require the same changes.

## I'm on a Windows Machine and when I try to exec onto a running container I get `stdin is not a tty`.
On Windows when utilizing Git Bash, you'll need to prefix interactive docker commands with `winpty`. E.g.

```bash
docker exec -it YOUR_PROJECT_NAME_php_1 bash
```

becomes

```
winpty docker exec -it YOUR_PROJECT_NAME_php_1 bash
```