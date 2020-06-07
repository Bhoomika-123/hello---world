# hello---world
public class HTMLDriverConcept {

	public static void main(String[] args) throws InterruptedException {
		
		
		System.setProperty("webdriver.chrome.driver", "C:\\\\Users\\\\Bhoomika\\\\Downloads\\\\chromedriver.exe");
		//WebDriver driver=new ChromeDriver();
		WebDriver driver=new HtmlUnitDriver();
		driver.manage().window().maximize();
		driver.manage().deleteAllCookies();
		
		driver.manage().timeouts().pageLoadTimeout(20, TimeUnit.SECONDS);
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.get("https://ui.freecrm.com/");
		
		System.out.println("Before log in the title is " +driver.getTitle());
		Thread.sleep(2000);
		
		driver.findElement(By.xpath("//input[contains(@type,'text')]")).sendKeys("mamtorabhoomika2110@gmail.com");
		driver.findElement(By.xpath("//input[contains(@type,'password')]")).sendKeys("Test@123");
		
driver.findElement(By.xpath("//div[contains(@class,'ui fluid large blue submit button')]")).click();
Thread.sleep(2000);
System.out.println("After log in the title is " +driver.getTitle());
		

	}

}
