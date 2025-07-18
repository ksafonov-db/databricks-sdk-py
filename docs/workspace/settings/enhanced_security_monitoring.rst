``w.settings.enhanced_security_monitoring``: Enhanced Security Monitoring
=========================================================================
.. currentmodule:: databricks.sdk.service.settings

.. py:class:: EnhancedSecurityMonitoringAPI

    Controls whether enhanced security monitoring is enabled for the current workspace. If the compliance
    security profile is enabled, this is automatically enabled. By default, it is disabled. However, if the
    compliance security profile is enabled, this is automatically enabled.

    If the compliance security profile is disabled, you can enable or disable this setting and it is not
    permanent.

    .. py:method:: get( [, etag: Optional[str]]) -> EnhancedSecurityMonitoringSetting

        Gets the enhanced security monitoring setting.

        :param etag: str (optional)
          etag used for versioning. The response is at least as fresh as the eTag provided. This is used for
          optimistic concurrency control as a way to help prevent simultaneous writes of a setting overwriting
          each other. It is strongly suggested that systems make use of the etag in the read -> delete pattern
          to perform setting deletions in order to avoid race conditions. That is, get an etag from a GET
          request, and pass it with the DELETE request to identify the rule set version you are deleting.

        :returns: :class:`EnhancedSecurityMonitoringSetting`
        

    .. py:method:: update(allow_missing: bool, setting: EnhancedSecurityMonitoringSetting, field_mask: str) -> EnhancedSecurityMonitoringSetting

        Updates the enhanced security monitoring setting for the workspace. A fresh etag needs to be provided
        in `PATCH` requests (as part of the setting field). The etag can be retrieved by making a `GET`
        request before the `PATCH` request. If the setting is updated concurrently, `PATCH` fails with 409 and
        the request must be retried by using the fresh etag in the 409 response.

        :param allow_missing: bool
          This should always be set to true for Settings API. Added for AIP compliance.
        :param setting: :class:`EnhancedSecurityMonitoringSetting`
        :param field_mask: str
          The field mask must be a single string, with multiple fields separated by commas (no spaces). The
          field path is relative to the resource object, using a dot (`.`) to navigate sub-fields (e.g.,
          `author.given_name`). Specification of elements in sequence or map fields is not allowed, as only
          the entire collection field can be specified. Field names must exactly match the resource field
          names.

          A field mask of `*` indicates full replacement. It’s recommended to always explicitly list the
          fields being updated and avoid using `*` wildcards, as it can lead to unintended results if the API
          changes in the future.

        :returns: :class:`EnhancedSecurityMonitoringSetting`
        