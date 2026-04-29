function sendBulkEmails() {
  var sheet = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet();
  var lastRow = sheet.getLastRow();

  var subject = "Paste your subject";

  for (var i = 2; i <= lastRow; i++) {
    var name  = sheet.getRange(i, 1).getValue(); // Column A = NAME
    var email = sheet.getRange(i, 2).getValue(); // Column B = MAIL

    var body = "Dear " + name + ",\n\n" +
               "I hope you are doing well.\n\n" +
               "Warm regards,\n" +
               "write your name\n" +
               "your agency name";

    if (email) {
      GmailApp.sendEmail(email, subject, body);
      Logger.log("Sent to: " + name + " - " + email);
    }
  }

  SpreadsheetApp.getUi().alert("✅ All emails sent successfully!");
}
