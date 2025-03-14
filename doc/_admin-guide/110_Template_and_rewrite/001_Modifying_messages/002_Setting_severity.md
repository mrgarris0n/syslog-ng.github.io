---
title: Setting severity with the set-severity() rewrite function
short_title: Setting severity
id: adm-temp-severity
description: >-
    It is possible to configure the severity field with the [[set-severity()|adm-temp-severity]]
    rewrite function. When configured, the [[set-severity()|adm-temp-severity]] rewrite function
    will only rewrite the ${SEVERITY} field in the message to the first
    parameter value specified in the function.
---

{% include doc/admin-guide/notes/not-valid-param.md %}

**Declaration**

```config
rewrite <name_of_the_rule> {
    set-severity("severity string or number");
};
```

## Parameters

The [[set-severity()|adm-temp-severity]] rewrite function has a single, mandatory parameter
that can be defined as follows:

```config
set-severity( "parameter1" );
```

## Accepted values

The [[set-severity()|adm-temp-severity]] rewrite function accepts the following values:

{% include doc/admin-guide/options/filter-severity.md %}

### Example usage for the set-severity() rewrite function

The following examples can be used in production for the set-severity()
rewrite function.

**Example using string:**

```config
rewrite {
    set-severity("info");
};
```

**Example using numeric string:**

```config
rewrite {
    set-severity(6);
};
```

**Example using template:**

```config
rewrite {
    set-severity("${.json.severity}");
};
```

{% include doc/admin-guide/warnings/dotdot-stringonly.md %}
