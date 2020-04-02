# Mobile
https://www.codota.com/code/java/methods/io.appium.java_client.touch.offset.PointOption/point

 String text ="some text";
                MobileDriverProvider.getAppiumDriver().findElement(MobileBy
                .AndroidUIAutomator("new UiScrollable(new UiSelector()).setAsVerticalList().scrollIntoView("
                        + "new UiSelector().text(\""+text+"\"));"));
                        



Driver.swipe(...)
public static void swipe(int startX,int startY, int endX, int endY){
  log.info("scroll from : startX " +startX + ", startY "+ startY+ ", to  endX "+ endX+ ",endY "+ endY);
  try {
    TouchAction touchAction = new TouchAction(driver);
    PointOption pointStart = PointOption.point(startX, startY);
    PointOption pointEnd = PointOption.point(endX, endY);
    WaitOptions waitOption = WaitOptions.waitOptions(Duration.ofMillis(1000));
    touchAction.press(pointStart).waitAction(waitOption).moveTo(pointEnd).release().perform();
  }catch (Exception e){
    log.error("scroll from : startX " +startX + ", startY "+ startY+ ", to  endX "+ endX+ ",endY "+ endY);
    e.printStackTrace();
  }
}
                        
