# Se--Pop-up

package SeleniumSession;

import org.openqa.selenium.Alert;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;

public class AlerPopupHandle {

	public static void main(String[] args) throws InterruptedException {

		System.setProperty("webdriver.chrome.driver", "C:\\Users\\Arun\\eclipse-workspace\\Selenium\\lib\\chromedrivers\\chromedriver.exe");
		WebDriver driver = new  ChromeDriver();
		
		driver.get("https://mail.rediff.com/cgi-bin/login.cgi");
		
		driver.findElement(By.xpath("//input[@title='Sign in']")).click();
		
		Thread.sleep(5000);
		
		Alert alert = driver.switchTo().alert();
		
		
		System.out.println(alert.getText());
		
		
		alert.accept();
		
		//alert.dismiss(); // to click cancel button
		
		

	}

}

