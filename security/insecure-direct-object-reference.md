# Insecure Direct Object Reference

API resources' identifiers should be unpredictable.

> For instance, MongoDB identifiers are not unpredictable and can be guessed.

{% hint style="warning" %}
An unpredictable identifier is not enough to secure the access to the resources.
{% endhint %}

{% hint style="success" %}
The API should verify access permissions for each resource.
{% endhint %}



