package paginaDePagos;
import static org.junit.Assert.assertTrue;

import java.util.concurrent.TimeUnit;

import org.junit.Before;
import org.junit.Test;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

public class ingresoregistro {
	
	By registerLinkLocator = By.linkText("Sign in");
	
	By usernameLocator = By.id("email_create");
	
	By findElement = By.cssSelector("#SubmitCreate > span");
	
	By homePageLocator = By.cssSelector(".page-heading");
	
	
	//ingreso de datos
		By firstname= By.id("customer_firstname");
		By Lastname = By.id("customer_lastname");
		By passLocator = By.name("passwd");
		By dia = By.name("days");
		By mes = By.name("months");
		By año = By.name("years");
		By SigNewsletter= By.id("uniform-newsletter");
		By Receivespecialoffersfromourpartners= By.id("optin");
		By Company= By.id("company");
		By Address= By.id("address1");
		By City = By.id("city");
		By ZipPostal = By.id("postcode");
		By State = By.id("id_state");
		By Country = By.id("id_country");
		By phoneMobile = By.id("phone_mobile");
		By Mobile = By.id("phone");
		By Assignanaddressaliasfuturereference = By.id("alias");
		By registerf1 =By.tagName("submitAccount");
		
		
	//Sign up for our Newsletter!alias

	private WebDriver driver;
	
	@Before
	public void setUp() throws Exception {
		System.setProperty("webdriver.chrome.driver", "./src/test/resources/chromedriver/chromedriver.exe");
		driver = new ChromeDriver();
		driver.manage().window().maximize();
		driver.get("http://automationpractice.com/index.php");
		}
	
	

	    @Test
	    public void testGooglePage()throws InterruptedException {
		
	  
		
		
		
		if(driver.findElement(registerLinkLocator).isDisplayed()) {
			driver.findElement(registerLinkLocator).click();
			driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);
			
			System.out.println("ingresado correctamente"); 
			driver.findElement(usernameLocator).isDisplayed();
			
			driver.findElement(usernameLocator).sendKeys("quality12ad13@mgmail.com");
			
			driver.findElement(By.cssSelector("#SubmitCreate > span")).click();
			driver.manage().timeouts().implicitlyWait(15, TimeUnit.SECONDS);
			System.out.println("ingresado correctamente2"); 
			assertTrue(driver.findElement(homePageLocator).isDisplayed());
			System.out.println("ingresado correctamente3"); 
			
			driver.findElement(firstname).sendKeys("john");
			driver.manage().timeouts().implicitlyWait(15, TimeUnit.SECONDS);
			System.out.println("imgreso satifatorio nombre"); 
			
			
			driver.findElement(Lastname).sendKeys("ALEXANDER");
			driver.manage().timeouts().implicitlyWait(15, TimeUnit.SECONDS);
			System.out.println("imgreso satifatorio nombre"); 
			
			
			
			driver.findElement(passLocator).sendKeys("1222@Alexander1234");
			driver.manage().timeouts().implicitlyWait(15, TimeUnit.SECONDS);
			System.out.println("imgreso satifatorio paswor ok"); 
			
			driver.findElement(dia).sendKeys("12");
			driver.manage().timeouts().implicitlyWait(15, TimeUnit.SECONDS);
			System.out.println("imgreso satifatorio paswor dia 12 ok"); 
			
			driver.findElement(mes).sendKeys("September");
			driver.manage().timeouts().implicitlyWait(15, TimeUnit.SECONDS);
			System.out.println("imgreso satifatorio paswor mes  ok"); 
			
			
			driver.findElement(año).sendKeys("1985");
			driver.manage().timeouts().implicitlyWait(15, TimeUnit.SECONDS);
			System.out.println("imgreso satifatorio paswor año  ok"); 
			
			driver.findElement(SigNewsletter).click();
			driver.manage().timeouts().implicitlyWait(15, TimeUnit.SECONDS);
			
			driver.findElement(Receivespecialoffersfromourpartners).click();
			driver.manage().timeouts().implicitlyWait(15, TimeUnit.SECONDS);
			
			driver.findElement(Company).sendKeys("diebol");
			driver.manage().timeouts().implicitlyWait(15, TimeUnit.SECONDS);
			System.out.println("imgreso satifatorio paswor año  ok"); 
			
			driver.findElement(Address).sendKeys("calle 26 # 25-21");
			driver.manage().timeouts().implicitlyWait(15, TimeUnit.SECONDS);
			System.out.println("imgreso satifatorio paswor año  ok"); 
			
			driver.findElement(City).sendKeys("Bogota");
			driver.manage().timeouts().implicitlyWait(15, TimeUnit.SECONDS);
			System.out.println("imgreso satifatorio paswor año  ok"); 
			
			
			
			
			driver.findElement(State).sendKeys("Vermont");
			driver.manage().timeouts().implicitlyWait(15, TimeUnit.SECONDS);
			System.out.println("imgreso satifatorio paswor año  ok"); 
			
			driver.findElement(ZipPostal).sendKeys("00000");
			driver.manage().timeouts().implicitlyWait(15, TimeUnit.SECONDS);
			System.out.println("imgreso satifatorio paswor año  ok"); 

			driver.findElement(Country).sendKeys("usne");
			driver.manage().timeouts().implicitlyWait(15, TimeUnit.SECONDS);
			System.out.println("imgreso satifatorio paswor año  ok"); 
			
			driver.findElement(phoneMobile).sendKeys("35059022707");
			driver.manage().timeouts().implicitlyWait(15, TimeUnit.SECONDS);
			System.out.println("imgreso satifatorio paswor año  ok"); 
			
			driver.findElement(Mobile).sendKeys("35059027207");
			driver.manage().timeouts().implicitlyWait(15, TimeUnit.SECONDS);
			System.out.println("imgreso satifatorio paswor año  ok"); 
			
			driver.findElement(Assignanaddressaliasfuturereference).sendKeys("jf35059027207");
			driver.manage().timeouts().implicitlyWait(15, TimeUnit.SECONDS);
			System.out.println("imgreso satifatorio paswor año  ok"); 
			
			driver.findElement(By.cssSelector("#submitAccount > span")).click();
			driver.manage().timeouts().implicitlyWait(15, TimeUnit.SECONDS);

			
			
		}else {
			System.out.println("ingresado  ja correctamente4"); 
					System.out.print("Re*as not found");
					
	  }
		
	}

		
}
