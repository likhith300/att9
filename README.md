package TEST22;
import java.util.List;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
public class Week9 {
public static void main(String[] args) {
	System.setProperty("webdriver.chrome.driver","C:\\Users\\aksha\\Downloads\\chromedriver-win64\\chromedriver-win64\\chromedriver.exe");
	
	WebDriver driver=new ChromeDriver();
driver.manage().window().maximize();
driver.get("https://www.justdial.com/Hyderabad/Bakeries/nct-10033880");
List<WebElement> m = driver.findElements(By.xpath("/html/body/div/section/section/div/div[5]"));
for(int i = 0; i< m.size(); i++) {
String s = m.get(i).getText();
System.out.println("Text is: " + s);
}
}
}
