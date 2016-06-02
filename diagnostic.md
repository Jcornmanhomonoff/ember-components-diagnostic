# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components.

    ```md
    The Listr client app interface
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember generate component my-ap
    ```

1.  What files are edited to produce a component, and what are their
    responsibilities?

    ```md
    Template: dynamically renders data
    Component:
    Route: provide route for view state

    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` path. What is
    the syntax for loading this component inside that template?

    ```html
    {{#each model as |contact|}}
      {{my-contact contacts=contact}}
    {{/each}}
    ```

    Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    {{#each contact.my-phone as |item|}}
      {{my-contact/my-phone tagName='li' my-phone=phone}}
    {{/each}}
    ```
