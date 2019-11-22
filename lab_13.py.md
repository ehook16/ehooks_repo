# ehooks_repo

	class delivery_personnel:
		def __init__(self, name, years_of_service, company, is_drone, zip_codes_covered):
			self.name = name
			self.years_of_service = years_of_service
			self.company = company
			self.is_drone = is_drone
			self.zip_codes_covered = zip_codes_covered

		def get_years(self):
			return(self.years_of_service)

		def get_company(self):
			return(self.company)

		def get_zip(self):
			return(self.zip_codes_covered)

		def set_years(self, d):
			self.years_of_service = d

		def set_company(self, d):
			self.company = d

		def set_zip(self, d):
			self.zip_codes_covered = d

		def deliver(self, zip_list):
			#if zip codes covered in list, remove zip code and print zip code
			for i in zip_list:
			 	if(i in self.zip_codes_covered):
					zip_list.remove(i)
				else:
			 		return(i)

			delivered_already = [i for i in zip_list if i in self.zip_codes_covered]
			print(delivered_already)

	def main():
		zip_list_1 = [44319, 44312, 44278]

		delivery_man = delivery_personnel(name = None, years_of_service = 3, company = "fedex" , is_drone = False, zip_codes_covered = [44319, 44278])

		delivery_man.deliver(zip_list_1)

	if __name__ == '__main__':
		main()
