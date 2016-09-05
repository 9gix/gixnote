# Long Text Splitter (Lazy Split)

    def splitter(text, amount):
        for i in range(0,len(text),amount):
            yield(text[i:i+amount])

	message = """Lorem ipsum dolor sit amet, consectetur adipiscing elit.
	Nulla orci neque, Aliquam laoreet blandit nulla,
	nec fermentum orci euismod vitae.
	Vestibulum non nisi at leo rutrum imperdiet. """
	x = splitter(message,50)
	print x.next() # 1 - 50
	print x.next() # 51 - 100
