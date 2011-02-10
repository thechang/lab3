class Appointment < ActiveRecord::Base

    def Appointment.assignAppointment (medic_id, patient_id, begin_time, end_time)
	citanueva = Appointment.new
	citanueva.medic_id = medic_id
	citanueva.patient_id = patient_id
	citanueva.begin_time = begin_time
	citanueva.end_time = end_time
	citanueva.save
    end
    
    def Appointment.modifyAppointment (appointment_id, medic_id, begin_time, end_time)
	if (appointment_id != nil)
	  cita = Appointment.where(:id => appointment_id).first
	  cita.id = appointment_id
	  cita.medic_id = medic_id
	  cita.begin_time = begin_time
	  cita.end_time = end_time
	  cita.save
	else
	  puts "no existe ese id"
	end
    end
      
    def Appointment.deleteAppointment (appointment_id)
	cita = Appointment.where(:id => appointment_id).first
	if (cita == nil)
	   puts "este id de la cita no existe"
	else
	  Appointment.delete(cita.id)
	end
    end
  
end