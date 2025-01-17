.. _list_reports:

List Reports
============


It's a simple ListView / admin changelist like report to display data in a model.
It's quite similar to ReportView except there is no calculation by default.

Options:
--------

filters: a list of report_model fields to be used as filters.

.. code-block:: python

    class RequestLog(ListReportView):
        report_model = Request

        filters = ["method", "path", "user_agent", "user", "referer", "response"]


Would yield a form like this

.. image:: _static/list_view_form.png
  :width: 800
  :alt: ListReportView form
  :align: center


Check :ref:`filter_form_customization` To customize the form as you wish.
