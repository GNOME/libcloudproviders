Title: Integrating with cloud providers

Integration with cloud providers can be achieved by fetching a list of exported
cloud provider accounts using [method@Collector.get_providers]. This function returns
a list of [class@Provider] objects that can then be used to obtain details about
the providers. Each [class@Provider] holds a list of [class@Account]
that can be query using [method@Provider.get_accounts].

To get notified about changes in either the [class@Provider] or each of
their [class@Account] you can connect to the "notify::" signal of
each of their properties. Any UI elements should be updated after receiving
this signal.

Besides the account details, [class@Account] may also export a [class@Gio.MenuModel] and a [iface@Gio.ActionGroup]
to provide actions that are related with the account. Those can be obtained by calling
[method@Account.get_menu_model] and [method@Account.get_action_group].
