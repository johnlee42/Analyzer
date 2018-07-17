# Analyzer
analyzer
基于ik analyzer可以实时加载扩展词典的ikanalyzer

//demo:
		StringReader input = new StringReader("需要分词的字符串");
		// 自定义配置文件，可以实时修改扩展词典
		MyConfiguration mycfg = new MyConfiguration();<p>
		String dicPath = "home/files/ectdic/dictionary.dic";//utf-8 无bom
		mycfg.setExtDictionarys(dicPath);
		IKSegmenter ikSeg = new IKSegmenter(input, mycfg, true);
		List<String> addrlist = new ArrayList<>();//
		List<Long> hashlist = new ArrayList<>();
		for (Lexeme lexeme = ikSeg.next(); lexeme != null; lexeme = ikSeg.next()) {
			System.out.print(lexeme.getLexemeText().toString());//提取出来的字符串
			}
		}
