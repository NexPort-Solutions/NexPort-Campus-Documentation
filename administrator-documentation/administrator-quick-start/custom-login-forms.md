# Custom Login Forms

Some partners may want to provide a custom login form. In order to do this you need to know the "Short Name" for your organization. This can be found on the [Organization Dashboard](../administrator-reference/campus-management/dashboard.md).

## Sample Form

<pre class="language-html" data-line-numbers data-full-width="true"><code class="lang-html">&#x3C;form id="loginForm" action="https://www.nexportcampus.com/<a data-footnote-ref href="#user-content-fn-1">ORGSHORTNAME</a>/Home/Login.nex" method="post">
&#x3C;fieldset >
        &#x3C;legend>Please Sign In...&#x3C;/legend>
        

        &#x3C;div class="layout-fixed">
            &#x3C;div class="col-left width-120 right">&#x3C;label for="username">Login:&#x3C;/label>&#x3C;/div>
            &#x3C;div class="col-main last">
                &#x3C;input id="username" name="username" type="text" >
           &#x3C;/div>
        &#x3C;/div>

        &#x3C;div class="layout-fixed">
            &#x3C;div class="col-left width-120 right">&#x3C;label for="password">Password:&#x3C;/label>&#x3C;/div>
            &#x3C;div class="col-main last">
                &#x3C;input id="password" name="password" type="password" >
            &#x3C;/div>
        &#x3C;/div>
        
            <a data-footnote-ref href="#user-content-fn-2">&#x3C;input type="hidden" name="authenticator" value="a92287a9-d2aa-46a4-8662-9ccd3de1e0e2"></a>

        &#x3C;div class="layout-fixed">
            &#x3C;div class="col-left width-120 right">
                &#x3C;input id="staySignedIn" type="checkbox" value="true" name="RememberMe" checked="checked">
            &#x3C;/div>
            &#x3C;div class="col-main last">
                &#x3C;label for="staySignedIn">Stay Signed In&#x3C;/label>
            &#x3C;/div>
        &#x3C;/div>

        &#x3C;div class="layout-fixed">
            &#x3C;div class="col-left width-120">&#x26;nbsp;&#x3C;/div>
            &#x3C;div class="col-main last">
                &#x3C;button id="loginButton" type="submit">Sign In&#x3C;/button>
            &#x3C;/div>
        &#x3C;/div>


        &#x3C;div class="layout-fixed" id="cookies-disabled-warning" style="display: none;">
            &#x3C;div class="col-left width-120 right">&#x3C;/div>
            &#x3C;div class="col-main last error">You must have cookies enabled in your browser to login&#x3C;/div>
        &#x3C;/div>
    &#x3C;/fieldset>
    &#x3C;/form>
</code></pre>

## Form Fields

| Field Name    | Description                                                      | Required/Optional |
| ------------- | ---------------------------------------------------------------- | ----------------- |
| username      | The nexport username of the student                              | required          |
| password      | Password of the student                                          | required          |
| authenticator | <p>Must be:<br><em>a92287a9-d2aa-46a4-8662-9ccd3de1e0e2</em></p> | required          |



[^1]: Use the organization short name from your nexport organization

[^2]: This input is required
