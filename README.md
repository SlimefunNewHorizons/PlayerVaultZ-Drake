# PlayerVaultZ-Drake (archived)

> **Superseded.** DrakesCraft now runs the unmodified upstream **PlayerVaultZ 1.3.0** by Rugzy
> ([Modrinth](https://modrinth.com/plugin/dJVm9lDf), MIT). Upstream 1.3.0 fixes the Quick Pick duplication
> this patch targeted, plus the navigation-bar duplication and silent save failures. Get it from Modrinth.

## History

The patch was built on PlayerVaultZ 1.1.0. Quick Pick removed items from `VaultPage#getItems()` (a copy), so the
persistent slot never changed and the item could be duplicated. The patch mutated the real slot through
`VaultPage#setItem`, compared full item stacks and blocked overlapping withdrawals. The source stays here for reference
(MIT, same as upstream); see `COMPILAR.md` to rebuild it against the original 1.1.0 jar (SHA-256
`F7225476AF8551898FA468112465C56C941E15185377B9690D642D7E28000CFB`, verified against Modrinth).

## License

MIT. Original work © Rugzy; patch by DrakesCraft Labs.
