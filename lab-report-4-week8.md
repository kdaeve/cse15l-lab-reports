# CSE Lab Report4

## Repo Links:  
[Mine](https://github.com/kdaeve/CSE15L-RoseateSpoonbill)  
[Other Group's](https://github.com/Shree-G/markdown-parse)  

## MarkdownParseTest Snippet Test Code:
```
    @Test
    public void snippet1() throws IOException{
        Path fileName = Path.of("snippet1.md");
	    String contents = Files.readString(fileName);
        ArrayList<String> links = MarkdownParse.getLinks(contents);
        ArrayList<String> expected = new ArrayList<>();
        expected.add("%60google.com");
        expected.add("google.com");
        expected.add("ucsd.edu");
        assertEquals(expected, links);
    }

    @Test
    public void snippet2() throws IOException{
        Path fileName = Path.of("snippet2.md");
	    String contents = Files.readString(fileName);
        ArrayList<String> links = MarkdownParse.getLinks(contents);
        ArrayList<String> expected = new ArrayList<>();
        expected.add("a.com");
        expected.add("a.com(())");
        expected.add("example.com");
        assertEquals(expected, links);
    }

    @Test
    public void snippet3() throws IOException{
        Path fileName = Path.of("snippet3.md");
	    String contents = Files.readString(fileName);
        ArrayList<String> links = MarkdownParse.getLinks(contents);
        ArrayList<String> expected = new ArrayList<>();
        expected.add("https://ucsd-cse15l-w22.github.io/");
        assertEquals(expected, links);
    }
```

## Expected Results:  
- Snippet1:[%60google.com, google.com, ucsd.edu]

## Snippet Fail of My Code  
Snippet 1 JUnitFail:  
![Image](images/lab-report4/s1JunitFail.png)  

Snippet 2 JUnitFail: 
![Image](images/lab-report4/s2JunitFail.png) 

Snippet 3 JUnitFail: 
![Image](images/lab-report4/s3JunitFail.png) 

## Snippet Fail of Other Group's Code  
Snippet 1 JUnitFail:  
![Image](images/lab-report4/Os1JunitFail.png)  

Snippet 2 JUnitFail: 
![Image](images/lab-report4/Os2JunitFail.png) 

Snippet 3 JUnitFail: 
![Image](images/lab-report4/Os3JunitFail.png) 

## Can the program be fixed in <10 lines?  
### Snippet 1:

### Snippet 2:

### Snippet 3: