# GoogleTranslateWidgetTesting

Working with a client and hit some issues with thier use of Google Translate Widget
Found Issue https://groups.google.com/forum/#!topic/accessible/aq9VKcq9YVw logged back on June, 22 2016
origianl repro location was apparently impacted by a WordPress upgrade, secondary repro on http://www.csulb.edu/  appears to have been modified to work around Googles issues.

Code from the CSULB site:
'''html
<div id="google_translate_widget_element">'
  <div class="skiptranslate goog-te-gadget" dir="ltr" style="">
    <div id=":0.targetLanguage" class="goog-te-gadget-simple" style="white-space: nowrap;">
      <img src="https://www.google.com/images/cleardot.gif" class="goog-te-gadget-icon" alt="" style="background-image: url(&quot;https://translate.googleapis.com/translate_static/img/te_ctrl3.gif&quot;); background-position: -65px 0px;">
      <span style="vertical-align: middle;">
     <a aria-haspopup="true" class="goog-te-menu-value" href="javascript:void(0)" tabindex="0">
        <span>Select Language</span>
        <img src="https://www.google.com/images/cleardot.gif" alt="" width="1" height="1">
        <span style="border-left: 1px solid rgb(187, 187, 187);">​</span>
        <img src="https://www.google.com/images/cleardot.gif" alt="" width="1" height="1"><span aria-hidden="true" style="color: rgb(155, 155, 155);">▼</span>
        </a>
      </span>
    </div>
  </div>
</div>
'''


on another site I found the following code...

'''html
<div id="google_translate_element">
  <div class="skiptranslate goog-te-gadget" dir="ltr" style="">
    <div id=":0.targetLanguage">
      <select class="goog-te-combo" aria-label="Language Translate Widget" id="translateID">
        <option value="">Select Language</option>
        <option value="af">Afrikaans</option>
        <option value="sq">Albanian</option>
        ...
        <option value="zu">Zulu</option>
      </select>
    </div>Powered by <span style="white-space:nowrap">
    <a class="goog-logo-link" href="https://translate.google.com" target="_blank">
      <img src="https://www.gstatic.com/images/branding/googlelogo/1x/googlelogo_color_42x16dp.png" width="37px" height="14px" style="padding-right: 3px" alt="Google Translate">Translate</a>
    </span>
  </div>
</div>
'''

Creating this to test with the default code provided by Google via https://translate.google.com/manager/website/?hl=en
