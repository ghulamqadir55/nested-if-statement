        import io.appium.java_client.android.AndroidDriver;
        import io.appium.java_client.remote.MobileCapabilityType;
        import org.openqa.selenium.By;
        import org.openqa.selenium.remote.DesiredCapabilities;

        import java.net.MalformedURLException;
        import java.net.URL;

        class AppiumDemo {

         public static void main(String[] args) throws MalformedURLException, InterruptedException {

        DesiredCapabilities dc = new DesiredCapabilities();

        driver.findElement(By.id("com.google.android.calculator:id/digit_5")).click();
        driver.findElement(By.id("com.google.android.calculator:id/op_add")).click();
        driver.findElement(By.id("com.google.android.calculator:id/digit_5")).click();
        driver.findElement(By.id("com.google.android.calculator:id/eq")).click();

        //System.out.println(Result);
        if ( driver.findElement(By.id("com.google.android.calculator:id/result_final")).getText().equals("10")) {
            System.out.println("Pass");
            driver.findElement(By.id("com.google.android.calculator:id/op_add")).click();
            driver.findElement(By.id("com.google.android.calculator:id/digit_5")).click();
            driver.findElement(By.id("com.google.android.calculator:id/eq")).click();
            if ( driver.findElement(By.id("com.google.android.calculator:id/result_final")).getText().equals("15")) {
                System.out.println("output is inside second if");

            }

        } else {
            System.out.println("Failed");
        }

        Thread.sleep(10000);
        driver.quit();
      }
     }
